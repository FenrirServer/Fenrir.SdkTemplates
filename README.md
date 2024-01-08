# Cloud SDK Templates repo

This repository contains templates to generate Fenrir Cloud SDK from the [OpenAPI 3.0 Specification](https://github.com/fenrirServer/openapi)

## Currently generated SDKs

- [.NET](https://github.com/fenrirServer/Fenrir.Api.DotNet)
- [Python](https://github.com/fenrirServer/Fenrir.Api.Python) 
- TypeScript [WIP]


## Generating all SDKs

To generate csharp SDKs:

```bash
export SDK=csharp  # csharp, python

docker run -v ${PWD}:/local openapitools/openapi-generator-cli generate \
    -g ${SDK} \
    -c /local/configs/${SDK}.yaml \
    -t /local/templates/${SDK} \
    --openapi-normalizer SET_TAGS_FOR_ALL_OPERATIONS=fenrir \
    --ignore-file-override=/local/${SDK}.openapi-generator-ignore
```


## Contributing guide

Please inspect the respective README files for each respective SDK template.
