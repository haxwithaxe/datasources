A repository of data sources for use with Huginn or dashboards (or anything else). The focus is on unusual, underdocumented, and undocumented web APIs and data sources.

[TODO.md](TODO.md) has a list of data sources and APIs that don't have an entry yet but should and hopefully eventually will.

# Contributing
To add documentation for an API create a PR with a file in the following format with a meaningful name ending with `.md`.
```md
A short desctiption.
<URL of the service providing the data>

# Docs
<URL of the documentation if any>
<Your additional notes>
# Examples
## Example label
<Example notes>
### Request
\```
<Example request including required headers>
\```
### Response
\```
<Example response that goes with the request>
\```
## Another example label
...

Keywords: Example Keyword, Foo, Bar
```
