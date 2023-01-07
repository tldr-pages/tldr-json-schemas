# tldr-json-schemas

JSON schemas to describe command syntax and enable example parsing easily. Man
pages are unrealiable parsing source as they are for humans and not always
it's possible to standardize their format quickly.

## Problems solved by this project

- Create a standardized and reliable way to explain command's CLI in a
  language independent manner
- Resolve issue with interpreting joined short options: it's not clear without
  reading man page what `-ab` is:
  - two joined short options, or
  - one option with a sticked value

## How it works?

All JSON schemas map to the TlDr pages in the same locations. For instance
[`common/rm.yaml`](./common/rm.yaml) maps to [`common/rm.md`](https://github.com/tldr-pages/tldr/blob/main/pages/common/rm.md) and specifies how to interpret it's
options which allows TlDr clients validate CLI in CI.
