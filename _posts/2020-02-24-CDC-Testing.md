---
layout: post
title: /Notes/ Consumer-Driven Contract Testing
---

_Research into pact.io_

- Consumer-Driven Contracts (CDCs) are about the service-oriented relationship between services.
- Consumers drive what the provider's service level and interface is
  - Each consumer defines what it expects the provider to deliver and the provider has to do the checking.
  - Flow:
    1. Provider advertises an initial offer
    1. Consumer declares new expectations
    1. Provider ensures consumer expectations are met
    1. Integration occurs
- How does it work?
  1. Developer of consumer service writes a test
    - Test defines an interaction with a provider
    - Includes state provider should be in, body of the request and the expected response
  1. Based on the definition of the consumer test, Pact creates and spins up a provider stub against which the test executes
    - Output of this test is one or more JSON files - these are the contracts (the pacts)
  1. Contracts are passed on to provider service
    - via shared repo, etc
  1. Provider tests if their service still 'obeys' the contract set by the consumer
    - Provider runs its own verification tests against a real-life version of its service, using shared pact file
  1. If tests do not succeed, provider developers should notify consumer developers


[Baeldung Resource](https://www.baeldung.com/pact-junit-consumer-driven-contracts)

[CodeFresh Resource](https://codefresh.io/docker-tutorial/how-to-test-microservice-integration-with-pact/)