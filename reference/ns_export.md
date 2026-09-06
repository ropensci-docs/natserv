# Search exports

Search exports

## Usage

``` r
ns_export(
  text = NULL,
  text_adv = NULL,
  status = NULL,
  location = NULL,
  record_type = NULL,
  record_subtype = NULL,
  modified_since = NULL,
  format = "json",
  lang = "en",
  ...
)

ns_export_status(id, ...)
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

- record_type:

  (character) limit results by record type, one of "species" or
  "ecosystem"

- record_subtype:

  (character) limit results by record sub-type, one of: "class",
  "subclass", "formation", "division", "macrogroup", "group",
  "alliance", "association", "terrestrial_ecological_system"

- modified_since:

  (character) search for records modified since a given time. value must
  be a date and time with a UTC offset in ISO 8601 format. optional

- format:

  (character) output format, one of "json" or "xlsx"

- lang:

  (character) language, one of "en", "es", or "fr"

- ...:

  Curl options passed on to
  [`verb-GET`](https://docs.ropensci.org/crul/reference/verb-GET.html)

- id:

  (character) a job id, from output of `ns_export()`

## Value

`ns_export()` returns a single character string (a job id)
`ns_export_status()` returns a list of metadata concerning the status of
the export

## References

https://explorer.natureserve.org/api-docs/

## Examples

``` r
if (FALSE) { # \dontrun{
x <- ns_export(text = "robin")
res <- ns_export_status(x)
str(res)
res$state
res$data$errorMessage
res$data$url

w <- ns_export(text_adv = list(searchToken = "western",
  matchAgainst="allScientificNames", operator="startsWith"))
m <- ns_export_status(w)
head(jsonlite::fromJSON(m$data$url))
} # }
```
