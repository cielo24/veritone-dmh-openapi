# Veritone DMH Assets API – OpenAPI Specification

This is a non-official OpenAPI/Swagger specification based on the official **Veritone DMH Assets API** documentation.
It is provided for convenience, making it easier to generate client libraries in multiple programming languages.

**NOTE:** This repository is not affiliated with Veritone. It exists solely to provide developers with a ready-to-use OpenAPI spec for the DMH Assets API, and to make it easier to generate clients or contribute improvements.

## Generating Client Code

There are multiple ways to generate client code from the OpenAPI specification, but we recommend using **Docker**.
This ensures you don’t need to install Java or other dependencies locally, and you get a consistent build environment.

Run the following command, replacing `LANGUAGE` with your target programming language:

```bash
docker run --rm \
  -v ${PWD}:/local openapitools/openapi-generator-cli generate \
  --package-name=veritone \
  -i /local/veritone.json \
  -g LANGUAGE \
  -o /local/veritone-LANGUAGE
```

**Example** for Python:

```bash
docker run --rm \
  -v ${PWD}:/local openapitools/openapi-generator-cli generate \
  --package-name=veritone \
  -i /local/veritone.json \
  -g python \
  -o /local/veritone-python
```

The `LANGUAGE` parameter can be any supported generator from OpenAPI Generator, such as:

> ada, android, csharp, dart, go, java, kotlin, php, python, ruby, scala, swift5, typescript, and more.

For a complete list, see the [OpenAPI Generator generators list](https://openapi-generator.tech/docs/generators/).
