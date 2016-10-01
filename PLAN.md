# Game Plan

### What is RAML?

[**RAML**](https://raml.org/) stands for **R**ESTful **A**PI **M**odeling **L**anguage. It's a way of describing an API in a machine-readable form. This allows us to let people [automatically generate clients](https://github.com/mulesoft/raml-client-generator) for the APIs, [among other things](https://raml.org/projects/projects).

There is another benefit of using RAML: its documentation features. It allows us to document the various aspects of the API in great detail.

### Why use RAML?

We can pair it with tools like [raml2`*`](https://github.com/raml2html/raml2obj) (where `*` is an output format) and have our documentation automatically generated and published for public consumption.

### Okay, what is the actual plan then?

We describe the APIs using [RAML 1.0](https://github.com/raml-org/raml-spec/blob/master/versions/raml-10/raml-10.md), and then we have [Travis CI](https://travis-ci.org/) ([documentation](https://docs.travis-ci.com/)) generate the documentation (and put it in the [`gh-pages` branch](https://github.com/r3c0d3x/chan-apis/tree/gh-pages)) whenever we push to the [`master` branch](https://github.com/r3c0d3x/chan-apis/tree/master) of the repo.

### Why does this project exist?

The original reason for creating this project was for the [Ayase framework](https://github.com/r3c0d3x/ayase), but besides that, the current documentation for most chan APIs is horrible, and they really leave developers in the dark.