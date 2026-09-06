# Get a summary of the upper level hierarchy for an Ecosystem record

Get a summary of the upper level hierarchy for an Ecosystem record

## Usage

``` r
ns_ecohier(uid, ...)
```

## Arguments

- uid:

  (character) A NatureServe taxon id (The taxon’s Element Global UID)

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
ns_ecohier("ELEMENT_GLOBAL.2.683060")
} # }
```
