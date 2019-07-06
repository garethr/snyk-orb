## Use Snyk with Circle CI

[![CircleCI](https://circleci.com/gh/garethr/snyk-orb.svg?style=svg)](https://circleci.com/gh/garethr/snyk-orb)

Using this Orb requires a [Snyk account](https://snyk.io/signup) and setting the `SNYK_TOKEN` environment variable in the relevant build.

```yaml
version: 2.1
orbs:
  snyk: garethr/snyk@0.3.0
jobs:
  build:
    docker:
      - image: "circleci/buildpack-deps:stretch"
    steps:
      - checkout
      - snyk/install_snyk
      - snyk/check_code_with_snyk
```

See the [full documentation on the Orb Registry](https://circleci.com/orbs/registry/orb/garethr/snyk).
