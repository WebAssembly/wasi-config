# `wasi-runtime-config`

A proposed [WebAssembly System Interface](https://github.com/WebAssembly/WASI) API.

### Current Phase

`wasi-runtime-config` is currently in [Phase 1](https://github.com/WebAssembly/WASI/blob/main/Proposals.md#phase-1---feature-proposal-cg).

### Champions

- [Dan Chiarlone](https://github.com/danbugs)
- [David Justice](https://github.com/devigned)
- [Jiaxiao Zhou](https://github.com/Mossaka)

### Phase 4 Advancement Criteria

`wasi-runtime-config` should have at least two implementations (i.e., from service providers, and or cloud providers), and, at the very minimum, pass the testsuite for Windows, Linux, and MacOS.

## Table of Contents

- [Introduction](#introduction)

### Introduction

The `wasi-runtime-config` world aim to provide a set of generic interfaces for dynamic configuration management systems. They are often the source of the configuration truth that lives in external services. Configuration values are often polled by the application for

1. toggling on/off feature flags
2. A/B testing
3. reading user allow/deny lists

and many more use cases.

### TODO

This readme needs to be expanded to cover a number of additional fields suggested in the [WASI Proposal template](https://github.com/WebAssembly/wasi-proposal-template).
