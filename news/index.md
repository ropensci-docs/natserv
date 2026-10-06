# Changelog

## natserv 1.0.0

CRAN release: 2020-05-16

#### BREAKING CHANGES

- All old functions are gone and have been replaced by new functions.
  NatureServe has released a new API and is ending support for the old
  one on 15 June 2020, so there’s no reason to support the old API. See
  the docs (<https://docs.ropensci.org/natserv/>) for example usage
  ([\#21](https://github.com/ropensci/natserv/issues/21))

## natserv 0.4.0

CRAN release: 2020-04-17

#### MINOR IMPROVEMENTS

- update vignette to use rmarkdown style, make sure vignette has a title
  ([\#20](https://github.com/ropensci/natserv/issues/20))

## natserv 0.3.0

CRAN release: 2019-01-23

#### NEW FEATURES

- gains a vignette: “Introduction to `natserve` - An R package to wrap
  NatureServe’s database API from rOpenSci”
  ([\#6](https://github.com/ropensci/natserv/issues/6))
  ([\#16](https://github.com/ropensci/natserv/issues/16)) all work done
  by [@mairindeith](https://github.com/mairindeith) - thanks!

#### MINOR IMPROVEMENTS

- add `vcr` for tests so that http requests are cached
  ([\#18](https://github.com/ropensci/natserv/issues/18))
- link to taxize book in readme and vignette
  ([\#15](https://github.com/ropensci/natserv/issues/15))
- improve failure behavior. the NatureServe API returns 200 on no result
  found, so we have to do gymnastics to catch that scenario
  ([\#9](https://github.com/ropensci/natserv/issues/9))

#### BUG FIXES

- bug in `ns_data()` fixed related to subnations
  ([\#10](https://github.com/ropensci/natserv/issues/10))
- a bunch of checks added within `ns_data()`, `ns_images()`, and
  `ns_search()` to catch common bad inputs to the functions
  ([\#11](https://github.com/ropensci/natserv/issues/11))
- fixed bug in internal function `check_uid()` that was throwing
  warnings in `ns_data()` when passing more than one input
  ([\#14](https://github.com/ropensci/natserv/issues/14))

## natserv 0.1.4

CRAN release: 2017-01-03

#### MINOR IMPROVEMENTS

- `natserv` now requires `crul` `>= 0.2.0`, which fixed URL encoding to
  make our work in `natserv` easier.

## natserv 0.1.0

CRAN release: 2016-12-15

#### NEW FEATURES

- released to CRAN
