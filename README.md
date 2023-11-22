# `wasi-runtime-config`

A proposed [WebAssembly System Interface](https://github.com/WebAssembly/WASI) API.

### Current Phase

`wasi-runtime-config` is currently in [Phase 1](https://github.com/WebAssembly/WASI/blob/main/Proposals.md#phase-1---feature-proposal-cg).

### Champions

- [Dan Chiarlone](https://github.com/danbugs)
- [David Justice](https://github.com/devigned)
- [Jiaxiao Zhou](https://github.com/Mossaka)

### Phase 4 Advancement Criteria

`wasi-runtime-config` should have at least two implementations (i.e., from service providers, and or
cloud providers), and, at the very minimum, pass the testsuite for Windows, Linux, and MacOS.

## Table of Contents

- [Introduction](#introduction)

### Introduction

The `wasi-runtime-config` world aim to provide a set of generic interfaces for providing
configuration to a component. Configuration values are often polled by the application for

1. Configuring the runtime behavior of a component. Yes, that sounds generic, but applications do
   all sorts of crazy things with configuration values! Calling entirely different branches of code,
   setting upstream URLs or services, configuring the number of threads to use, etc.
2. toggling on/off feature flags
3. A/B testing

and many more use cases.

### TODO

This readme needs to be expanded to cover a number of additional fields suggested in the [WASI
Proposal template](https://github.com/WebAssembly/wasi-proposal-template).
