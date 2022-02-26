## Example Consumer Mountebank

[![Build](https://github.com/pactflow/example-bi-directional-consumer-mountebank/actions/workflows/build.yml/badge.svg)](https://github.com/pactflow/example-bi-directional-consumer-mountebank/actions/workflows/build.yml)

This is an example of a Node consumer using Mountebank stubs, and using the Bi-Directional Contract Testing feature of [Pactflow](https://pactflow.io).

It implements a simple Product API client for the [Provider](https://github.com/pactflow/example-pactflow-example-provider-dredd) counterpart.

### Pre-requisites

**Software**:

* Tools listed at: https://docs.pactflow.io/docs/workshops/ci-cd/set-up-ci/prerequisites/
* A pactflow.io account with an valid [API token](https://docs.pactflow.io/docs/getting-started/#configuring-your-api-token)


#### Environment variables

To be able to run some of the commands locally, you will need to export the following environment variables into your shell:

* `PACT_BROKER_TOKEN`: a valid [API token](https://docs.pactflow.io/docs/getting-started/#configuring-your-api-token) for Pactflow
* `PACT_BROKER_BASE_URL`: a fully qualified domain name with protocol to your pact broker e.g. https://testdemo.pactflow.io
* `PACT_PROVIDER=pactflow-example-provider-dredd`: this changes the default provider to the Dredd based provider (https://github.com/pactflow/example-provider-dredd)
* `PACT_PROVIDER=pactflow-example-provider-postman`: ... Postman (https://github.com/pactflow/example-provider-postman)
* `PACT_PROVIDER=pactflow-example-provider-restassured`: ... Rest Assured (https://github.com/pactflow/example-provider-restassured)

See all bi-directional contract testing compatible provider [examples](https://docs.pactflow.io/docs/examples).

### Usage

* `make test` - run the pact test locally
* `make fake_ci` - run the CI process locally