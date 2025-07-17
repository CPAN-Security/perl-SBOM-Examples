# perl-SBOM-Examples

Examples of different SBOM files, for common use cases

## Requirements

- Native CPAN modules (already supported)
- Pre-resolved dependencies
- Services
- Local (system) packages
- Alien packages


## Dependencies

- Resolved CPAN dependencies (already supported)
- Included dependencies (pre-resolved)
  - CPAN
  - Non-CPAN (e.g. `libfoo.so` or `bootstrap.js`)
- Use Repology for finding local names based on requirements
- Report all packages and dependencies that were created/installed/deployed in an SBOM


# When should an SBOM file be created or updated?

When a field needs to be added, updated, or censored!


## Meta-metadata fields that always need to be updated

Reference: [Baseline SBOM Metadata](https://security.metacpan.org/docs/supplychain-sbom.html#environment-independent-baseline-attribute)

- SBOM Author
- SBOM Creation Timestamp
- SBOM Format
- SBOM Generation Tool
- SBOM Location (Authoritative)


## Basic [project information](https://security.metacpan.org/docs/supplychain-sbom.html#oss-project-environment) is initially declared

- Supplier Name
- Primary Component Name
- Version
- Included Dependencies (pre-resolved)

- Unique Product Identifier
- Purpose, Intended use
- Security contact
- Copyright Holder
- License

- Open Source Software Steward
- Intended for Commercial Activities

- Contribution Instructions


## When a dependency is vendored in (included, embedded) by the Maintainer, before publishing

All these refer to the metadata of the _included (pre-resolved) dependency_.

- Supplier Name
- Component Name
- Version

- Security contact
- License
- SBOM Location
- Download Location
- Cryptographic hashes

Note: Verify if the cryptographic hashes match the vendored in dependency!


## When a new project name is assigned for use in a package ecosystem

- Unique Product Identifier
- Download Location


### When a project is patched by a Patcher

- Component Name
- Version
- Security Contact
- Download Location
- Patch file (?)


### When a dependency is resolved by a Builder

- Dependencies (resolved)


### When a project is re-packaged by a Packager

- Component Name
- Version
- Cryptographic Hash
