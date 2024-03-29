# UseID Architecture
Background documentation and overview of the UseId architecture

## UseId project
> **Important:  This project has been discontinued**
​
This repository is part of the UseId project, that provided the BundesIdent mobile app.  You can find other repositories related to this project in the following list:
​
- Architecture
	- [Architecture](https://github.com/digitalservicebund/useid-architecture/tree/main): Documentation and overview of the UseId architecture
- Backend
	- [Backend](https://github.com/digitalservicebund/useid-backend-service): Kotlin service that acts as the backend for the mobile apps and eID-Service integration for eServices.
- eService
	- [eService-example](https://github.com/digitalservicebund/useid-eservice-example): An example application for an eService integrating with the UseId identity solution.
	- [eService-SDK](https://github.com/digitalservicebund/useid-eservice-sdk): Javascript SDK to easily integrate with the UseId identity solution.
- eID client (mobile app)
	- [iOS client for BundesIdent](https://github.com/digitalservicebund/useid-app-ios)
	- [Android client for BundesIdent](https://github.com/digitalservicebund/useid-app-android)
	- [AusweisApp2 Wrapper iOS](https://github.com/digitalservicebund/AusweisApp2Wrapper-iOS-SPM): Forked repository of the Governikus AusweisApp2 Wrapper for iOS

## Architecture Diagrams

See [diagrams/README.md](diagrams/README.md)

## Architecture Decision Records

The `doc/adr` directory contains [architecture decisions](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions).
For adding new records the [adr-tools](https://github.com/npryce/adr-tools) command-line tool is useful but not strictly necessary:

```bash
brew install adr-tools
```

## Identification Flows

The `flows` directory contains descriptions of the identification flows of the UseID identity solution
including [Mermaid sequence diagrams](https://mermaid-js.github.io/mermaid/#/sequenceDiagram). 

## Research

The `research` directory contains documentation on research conducted on specific topics. 

## Contributing

Everyone is welcome to contribute the development of this project. You can contribute by opening pull request,
providing documentation or answering questions or giving feedback. Please always follow the guidelines and our
[Code of Conduct](CODE_OF_CONDUCT.md).

## Contributing code

Open a pull request with your changes and it will be reviewed by someone from the team. When you submit a pull request,
you declare that you have the right to license your contribution to the DigitalService and the community.
By submitting the patch, you agree that your contributions are licensed under the MIT license.

Please make sure that your changes have been tested before submitting a pull request.


