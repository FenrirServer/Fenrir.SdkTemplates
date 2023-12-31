# Cloud SDK Templates repo

This repository contains templates to generate Fenrir Cloud SDK from the [OpenAPI 3.0 Specification](https://github.com/fenrirServer/openapi)

## Currently generated SDKs

- [.NET](https://github.com/fenrirServer/Fenrir.Api.DotNet)
- Python [WIP]
- TypeScript [WIP]


## Generating all SDKs

To generate csharp SDKs:

```bash
docker run -v ${PWD}:/local openapitools/openapi-generator-cli generate \
    -g csharp \
    -c /local/configs/csharp.yaml \
    -t /local/templates/csharp \
    --openapi-normalizer SET_TAGS_FOR_ALL_OPERATIONS=fenrir \
    --ignore-file-override=/local/csharp.openapi-generator-ignore
```


## Contributing guide

Please inspect the respective README files for each respective SDK template.
