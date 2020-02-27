# Test vectors

The following test vectors are provided to check your implementation of this spec.

The highest level vectors which will tell you whether you have everything working are:
The highest level vectors you need to be able to pass are:
- `box*.json`
- `unbox*.json`

The other test vectors are provided as stepping stones for imporant parts the spec:
- `derive_secret*.json` : deriving keys from the master `msg_key`
- `slot*.json` + `unslot*.json` : creating and reading from a `key_slot`
- `cloaked_id*.json` : creating a "cloaked" message id from and message which has an envelope

## Format

All test vectors follow the format:

```
{
  type: String,               // machine readable
  description: String,        // human readable
  input: {
    ...                       // base64 encoded properties
  },
  output: {
    ...                       // base64 encoded properties
  },
  error_code: (null|String)
}
```

Notes:
- where `input` / `output` format will depend on the `type`.
- if `error_code` is a `String` all attributes in `output` with be `null`
