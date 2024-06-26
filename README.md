# AliyunOpenAPI

[![Hex.pm](https://img.shields.io/hexpm/v/aliyun_open_api.svg)](https://hex.pm/packages/aliyun_open_api)

> An SDK builder for Aliyun / Alibaba Cloud OpenAPI.

This package is an SDK builder. It provides utilities to reduce the cost of creating an SDK, such as:

- building requests
- signing requests
- sending requests
- ...

And, this package was designed according to certain principles:

- It provides only low-level APIs.
- It doesn't touch the response body.
- It doesn't provide one-to-one mapping against all available APIs. See the reason in [FAQ](#faq).

## Notes

This package is still in its early stages, so it may still undergo significant changes, potentially leading to breaking changes.

## Installation

Add `:aliyun_open_api` to the list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:aliyun_open_api, "~> <version>"}
  ]
end
```

## Usage

For more information, see the [documentation](https://hexdocs.pm/aliyun_open_api/AliyunOpenAPI.html).

## FAQ

### Why not providing one-to-one mapping against all available APIs?

Because:

- It's hard to do the mapping automatically:
  - The official API documentation isn't structured data.
  - It's hard to parse and map them to API requests.
- It's hard to do all the mapping manually:
  - It's a tedius work.
  - It's error-prone.
- For an individual like me, this is a significant amount of work. I don't want to spend my time on such things.

And, in most real apps, it's rare that all available APIs are required. In general, only a few API are required. So, mapping what is required is acceptable.

The simpler, the better.

### Why not using a simple and short name?

I want to describe what a package does clearly and explicitly. The length of a name doesn't matter, as long as it is clear and explicit.

## License

[Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0)
