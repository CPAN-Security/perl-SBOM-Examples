# perl-SBOM-Examples

Examples of different SBOM files, for common use cases

## Situations where an SBOM file should be created or updated

### Meta-metadata fields that need to be updated always

[SBOM Metadata](https://security.metacpan.org/docs/supplychain-sbom.html#environment-independent-baseline-attribute)

- SBOM Author
- SBOM Creation Timestamp
- SBOM Format
- SBOM Generation Tool
- SBOM Location (Authoritative)
- SBOM 

### When basic [project information](https://security.metacpan.org/docs/supplychain-sbom.html#oss-project-environment) is declared

- Supplier Name
- Primary Component Name
- Version
- Dependencies (included)

- Copyright Holder
- License
- Security contact
- Unique Product Identifier
- Purpose, Intended use

- Open Source Software Steward
- Intended for commercial activities

- Contribution Instructions


### When a dependency is vendored in (included, embedded) by the Maintainer, before publishing

- Supplier Name
- Component Name
- Version

- Security contact
- License
- SBOM Location
- Download Location


### When a new project name is assigned for use in a package ecosystem

- Unique Product Identifier

### When a project is patched by a Patcher

- Component Name
- Version
- Security Contact

### When a dependency is resolved by a Builder

- Dependencies (resolved)

### When a project is re-packaged by a Packager

- Component Name
- Version
- Cryptographic Hash

