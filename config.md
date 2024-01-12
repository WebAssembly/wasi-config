# Runtime Config API

## Runtime Types

### `variant config-error`

An error type that encapsulates the different errors that can occur fetching config:

- `upstream(string)`: This indicates an error from an "upstream" config source. As this could be almost _anything_ (such as Vault, Kubernetes ConfigMaps, KeyValue buckets, etc), the error message is a string.
- `io(string)`: This indicates an error from an I/O operation. As this could be almost _anything_ (such as a file read, network connection, etc), the error message is a string. Depending on how this ends up being consumed, we may consider moving this to use the `wasi:io/error` type instead. For simplicity right now in supporting multiple implementations, it is being left as a string.


## Runtime Functions

## `get`

Gets a single opaque config value set at the given key if it exists

**Params:**

- `key`: A string key to fetch

**Returns:**

`result<option<list<u8>>, config-error>`

An opaque value if the key exists, otherwise `none`

## `get-all`

Gets all available configuration values

**Params:**

None

**Returns:**

`result<list<tuple<string, list<u8>>>, config-error>`

A list of key/value tuples
