# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [1.0.1] - 2024-01-07
### Changed
- [Breaking] Upgrade to Spring Boot v3.2.1 and SPQR v0.12.4 (graphql-java v21.3) [#140](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/140)

### Fixed
- Websocket handshake case-insensitive headers [#136](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/136)

## [1.0.0] - 2023-06-27
### Changed
- [Breaking] Upgrade to Spring Boot v3.1.1 and SPQR v0.12.3 (graphql-java v20.4) [#133](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/133)

## [0.0.8] - 2023-08-10
### Changed
- Upgrade to Spring Boot v2.7.14 and SPQR v0.12.3 (graphql-java v20.4)
- Better WebSocket configurability [#79](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/79)

## [0.0.7] - 2022-12-24
### Changed
- [Breaking] Upgrade to Spring Boot v2.7.6 and SPQR v0.12.1 (graphql-java v20.0) [#124](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/124)

## [0.0.6] - 2021-03-21
### Added
- Support subscriptions over SSE [#97](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/97)

### Changed
- [Breaking] Renamed all `Servlet*` classes to `Mvc*` (e.g. `ServletContextFactory` ➝ `MvcContextFactory`)
- [Breaking] Make async execution the default [#99](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/99)
- Rewrite the WebSocket-based subscriptions implementation [#98](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/98)

### Fixed
- Bean registration fails when it encounters a JDK Proxy [#100](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/100)

## [0.0.5] - 2021-02-09
### Added
- Support for Spring Data paging 🥳, with ot without Relay compatibility (thanks [@vjroby](https://github.com/vjroby)) [#2](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/2)
- Spring Security support in WebFlux (preserve Spring's subscriber context) 🥳 [#69](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/69) 
- Ability to choose a scheduler for `Mono`s

### Changed
- [Breaking] Upgraded to graphql-spqr 0.11.1 (with graphql-java v16.2)
- [Breaking] Upgraded to Spring Boot 2.4.2

### Fixed
- WebSockets (for subscriptions) now work correctly in Firefox [#54](https://github.com/vjroby)) [#9](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/54)
- Empty variables map handled correctly [#39](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/39)

## [0.0.4] - 2018-02-24
### Added
- WebFlux support (not yet for subscriptions) (thanks [@vjroby](https://github.com/vjroby)) [#9](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/9)
- Easier customization of GraphQL execution / error handling via `GraphQLExecutor` [#22](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/22)

### Changed
- Annotations are now in a separate module to enable lighter dependencies (thanks [@heruan](https://github.com/heruan)) [#6](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/6)

### Fixed
- `DataLoader` and global context now properly work in subscriptions [#19](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/19)

## [0.0.3] - 2018-12-14
### Added
- Full support for Apollo's graphql-ws protocol [#13](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/13)
- Easy way to inject custom global context [#11](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/11)
- Support for Reactor types (`Flux` and `Mono`) [#16](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/16)

### Changed
- [Breaking] Normalized all application properties. See [SpqrProperties](https://github.com/leangen/graphql-spqr-spring-boot-starter/blob/graphql-spqr-spring-boot-starter-v0.0.3/graphql-spqr-spring-boot-autoconfigure/src/main/java/io/leangen/graphql/spqr/spring/autoconfigure/SpqrProperties.java) for details.
- [Breaking] Default GUI endpoint changed from `/graphiql` to `/gui`
- Upgraded to [graphql-spqr 0.9.9](https://github.com/leangen/graphql-spqr/releases/tag/graphql-spqr-v0.9.9)
- GraphiQL replaced with [GraphQL Playground](https://github.com/prisma/graphql-playground) (might be revised later)

### Removed
- [Breaking] Removed `DefaultGlobalContext#getDataLoaders` as `DataLoader`s are now [accessible directly](https://github.com/graphql-java/graphql-java/pull/1263) 

### Fixed
- Proxied beans no longer cause an exception (enabling the usage of Spring Security, `@Transactional` etc) [#12](https://github.com/leangen/graphql-spqr-spring-boot-starter/issues/12)
