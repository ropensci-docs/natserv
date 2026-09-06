# Ecosystem search

Ecosystem search

## Usage

``` r
ns_search_eco(
  text = NULL,
  text_adv = NULL,
  status = NULL,
  location = NULL,
  ecosystem_taxonomy = NULL,
  record_subtype = NULL,
  modified_since = NULL,
  page = NULL,
  per_page = NULL,
  ...
)
```

## Arguments

- text:

  (character) basic text search, equiavalent to `text_adv` with
  `matchAgainst="allNames"` and `operator="similarTo"`

- text_adv:

  (list) advanced search, must specify the following three elements:
  `searchToken`, `matchAgainst`, and `operator`. see
  https://explorer.natureserve.org/api-docs/#\_advanced_text_search_parameter

- status:

  (character) conservation status, one of G1, G2, G3, G4, G5, GH, GX,
  GNR, GNA, GU. case insensitive

- location:

  (list) location, country and sub-country. specify either `nation` OR
  `nation` and `subnation`. each expects a two-letter ISO code

- ecosystem_taxonomy:

  (character) the classification code of the higher level (ancestor)
  ecosystem. E.g.'s: "1" (Class code), "1.B" (Subclass code), "1.B.2"
  (Formation code), "1.B.2.Nd" (Division code), "M886" (Macrogroup key),
  "G206" (Group key), "A3328" (Alliance Key)

- record_subtype:

  (character) limit results by record sub-type, one of: "class",
  "subclass", "formation", "division", "macrogroup", "group",
  "alliance", "association", "terrestrial_ecological_system"

- modified_since:

  (character) search for records modified since a given time. value must
  be a date and time with a UTC offset in ISO 8601 format. optional

- page:

  (integer) Zero-indexed page number; default: 0. optional

- per_page:

  (integer) Records per page; default: 20. optional

- ...:

  Curl options passed on to
  [`verb-GET`](https://docs.ropensci.org/crul/reference/verb-GET.html)

## References

https://explorer.natureserve.org/api-docs/

## See also

Other search:
[`ns_search_comb()`](https://docs.ropensci.org/natserv/reference/ns_search_comb.md),
[`ns_search_spp()`](https://docs.ropensci.org/natserv/reference/ns_search_spp.md)

## Examples

``` r
if (FALSE) { # \dontrun{
ns_search_eco(text = "robin")
ns_search_eco(text_adv = list(searchToken = "bird",
  matchAgainst = "allNames", operator="similarTo"))
ns_search_eco(status = "G1")
ns_search_eco(location = list(nation = "US"))
ns_search_eco(location = list(nation = "US", subnation = "VA"))
ns_search_eco(ecosystem_taxonomy = "M067")
ns_search_eco(record_subtype = "macrogroup")
ns_search_eco(modified_since = "2020-04-30T00:00:00+0000")
ns_search_eco(page = 0, per_page = 2)
} # }
```
