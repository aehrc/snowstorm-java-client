# Snowstorm Java Client

This project contains a Java client for Snowstorm generated using
the [openapi-generator-maven-plugin](https://github.com/OpenAPITools/openapi-generator/tree/master/modules/openapi-generator-maven-plugin). The aim of this project is to make Snowstorm's APIs easier to use from Java code without writing additional boilerplate.

## Getting Started
### Building
To build this project you'll need Java 17 or later and Maven 3 or later.

It can then be built by running 
```
mvn clean install
```

### Usage
To use the library include it in your Maven dependencies
```xml
    <dependency>
      <artifactId>snowstorm-java-client</artifactId>
      <groupId>au.csiro</groupId>
      <version>${snowstorm-java-client.version}</version>
    </dependency>
```
Then create a client and use it in the specific clients that divide up the Snowstorm API
```java
    @Autowired
    WebClient webclient;
    ...
    ApiClient client = new ApiClient(webclient);
    client.setBasePath("https://your.snowstorm/path");
    ConceptsApi conceptApi = new ConceptsApi(client);
    return api.findConcept(branch, id, "en").block();
```

Look in the generated package `au.csiro.snowstorm_client.api` for all the various API clients. These are divided based on the OpenAPI definition of the Snowstorm API.

## Versioning
Versioning is based on the Snowstorm release version.

## Contributing
If you are interested in contributing or would like a change, please check out the [contributing guide](CONTRIBUTING.md).

## Licensing
Distributed under the Apache 2.0 License. See [LICENSE.txt](LICENSE.txt) for more details.
