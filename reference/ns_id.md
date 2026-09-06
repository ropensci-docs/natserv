# Get taxon by uid

Get taxon by uid

## Usage

``` r
ns_id(uid, ...)
```

## Arguments

- uid:

  (character) A NatureServe taxon id (The taxon’s Element Global UID).
  required.

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
ns_id("ELEMENT_GLOBAL.2.154701")
} # }
```
