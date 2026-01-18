# Review list

This is the review list for [The List](/)

## Tools

### APIs

| Tool                                                    | Description                                                   | Replaced type-unsafe practices                                                               |
| ------------------------------------------------------- | ------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| [capnp](https://github.com/capnproto/go-capnproto2)     | Cap’n Proto serialization and RPC system for Go.              | Reflection-based field encoding/decoding in RPC or serialization. <!-- github.com/ufukty --> |
| [gqlgen](https://github.com/99designs/gqlgen)           | go generate based graphql server library                      | v <!-- github.com/ufukty -->                                                                 |
| [oapi-codegen](https://github.com/deepmap/oapi-codegen) | Generate Go client/server code from OpenAPI 3 specs.          | Runtime route dispatch & payload decoding with `reflect`. <!-- github.com/ufukty -->         |
| [protoc-gen-go-grpc](https://github.com/grpc/grpc-go)   | gRPC code generator for Go — creates client/server stubs.     | Dynamic service dispatch via reflection in RPC frameworks. <!-- github.com/ufukty -->        |
| [twirp](https://github.com/twitchtv/twirp)              | Simple RPC framework with generated code from `.proto` files. | Generic RPC routing and handler registration via reflection. <!-- github.com/ufukty -->      |

### Databases

| Tool                                 | Description                                                                          | Replaced type-unsafe practices                                                                |
| ------------------------------------ | ------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------- |
| [ent](https://github.com/ent/ent)    | An entity framework for Go: simple, yet powerful ORM for modeling and querying data. | Generic ORM field/column mapping via `reflect` (e.g., GORM-style). <!-- github.com/ufukty --> |
| [jet](https://github.com/go-jet/jet) | Type-safe SQL builder for Go with code generation from schema.                       | Reflection-based dynamic SQL builders. <!-- github.com/ufukty -->                             |
| [xo](https://github.com/xo/xo)       | Command-line tool to generate Go code from a database schema.                        | Dynamic ORM query building and result mapping. <!-- github.com/ufukty -->                     |

### De/serialization

| Tool                                                            | Description                                                     | Replaced type-unsafe practices                                                       |
| --------------------------------------------------------------- | --------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| [avrogen-go](https://github.com/actgardner/gogen-avro)          | Avro code generation for Go from Avro schema files.             | Reflection-based Avro decoding/encoding. <!-- github.com/ufukty -->                  |
| [easyjson](https://github.com/mailru/easyjson)                  | Fast JSON serializer for Go — reflectionless encoding/decoding. | `encoding/json` struct field scanning via reflection. <!-- github.com/ufukty -->     |
| [ffjson](https://github.com/pquerna/ffjson)                     | Faster JSON serialization for Go — generates static code.       | `encoding/json` reflection for marshaling/unmarshaling. <!-- github.com/ufukty -->   |
| [flatbuffers](https://github.com/google/flatbuffers)            | Memory-efficient serialization library with generated Go code.  | Generic serialization frameworks with reflection. <!-- github.com/ufukty -->         |
| [msgp](https://github.com/tinylib/msgp)                         | Code generator and runtime for MessagePack in Go.               | Dynamic serialization/deserialization frameworks. <!-- github.com/ufukty -->         |
| [protoc-gen-go](https://github.com/protocolbuffers/protobuf-go) | Go support for Protocol Buffers.                                | Generic serialization frameworks that rely on reflection. <!-- github.com/ufukty --> |

### Dependency Injection and Wiring

| Tool                                         | Description                                  | Replaced type-unsafe practices                                                               |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------------------------------------------------------- |
| [genny](https://github.com/cheekybits/genny) | Code generation for generic data structures. | Reflection-based generic containers and utils. <!-- github.com/ufukty -->                    |
| [wire](https://github.com/google/wire)       | Compile-time dependency injection for Go.    | Runtime DI containers using reflection to construct dependencies. <!-- github.com/ufukty --> |

### Testing and Mocks

| Tool                                                           | Description                                                              | Replaced type-unsafe practices                                                                      |
| -------------------------------------------------------------- | ------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- |
| [counterfeiter](https://github.com/maxbrunsfeld/counterfeiter) | Generates Go interfaces and their fakes.                                 | Reflection-based fake object creation. <!-- github.com/ufukty -->                                   |
| [mockery](https://github.com/vektra/mockery)                   | A mock code autogenerator for Go interfaces.                             | Reflection-based mocks that inspect method sets at runtime. <!-- github.com/ufukty -->              |
| [moq](https://github.com/matryer/moq)                          | Interface mocking tool for Go generate tests without hand-written mocks. | Reflection-driven mock frameworks that dynamically implement interfaces. <!-- github.com/ufukty --> |

### Enums / Code Helpers

| Tool                                         | Description                                                                            | Replaced type-unsafe practices                                                      |
| -------------------------------------------- | -------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| [enumer](https://github.com/dmarkham/enumer) | Code generation for Go enums with Stringer-like methods, JSON, text marshal/unmarshal. | Generic enum-to-string mappers using reflection or maps. <!-- github.com/ufukty --> |
| [go-enum](https://github.com/abice/go-enum)  | Generates enums from Go comments and type declarations.                                | Runtime enum parsing via reflection. <!-- github.com/ufukty -->                     |

### Validation

| Tool                                                                   | Description                                                                           | Replaced type-unsafe practices                                                                          |
| ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| [protoc-gen-validate](https://github.com/bufbuild/protoc-gen-validate) | Protocol Buffer codegen for message validation.                                       | Reflection-based validation frameworks that iterate over fields dynamically. <!-- github.com/ufukty --> |
| [validate](https://github.com/go-playground/validator)                 | With codegen wrappers, generates validation functions instead of runtime tag parsing. | Reflection-based tag scanning in validation. <!-- github.com/ufukty -->                                 |
