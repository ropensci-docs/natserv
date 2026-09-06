# Get taxon by uid, id, or elCode

Get taxon by uid, id, or elCode

## Usage

``` r
ns_altid(uid = NULL, id = NULL, el_code = NULL, ...)
```

## Arguments

- uid:

  (character) A NatureServe taxon id (The taxon’s Element Global UID)

- id:

  The primary key value (ELEMENT_GLOBAL_ID) of the record within Central
  Biotics

- el_code:

  The Biotics Element Code (ELCODE_BCD) of the record

- ...:

  Curl options passed on to
  [`verb-GET`](https://docs.ropensci.org/crul/reference/verb-GET.html)

## Value

A list with lots of elements

## Details

see https://explorer.natureserve.org/api-docs/#\_taxon_data_model for
details on the response data

## References

https://explorer.natureserve.org/api-docs/

## Examples

``` r
if (FALSE) { # \dontrun{
ns_altid(uid = "ELEMENT_GLOBAL.2.154701")
ns_altid(id = "154701")
ns_altid(el_code = "PDRAN0F010")
} # }
```
