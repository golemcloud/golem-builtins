# Golem built-ins

This repository stores immutable GitHub Release assets for Golem's built-in tools and plugins.

Component source, build definitions, compatibility code, tests, license generation, and publishing automation live in the [golem repository](https://github.com/golemcloud/golem). Keeping source there lets built-ins use the matching Golem SDK and build toolchain without introducing a release dependency cycle.

Release tags use `<component>-v<artifact-version>`. Each release contains the component WASM, its SHA-256 file, build provenance, and applicable license notices and SPDX SBOMs. Published tags and assets are immutable; changed bytes require a new artifact version.

The registry service downloads the exact URLs and checksums recorded in `golem/builtin-artifacts.json` and caches them locally before provisioning.
