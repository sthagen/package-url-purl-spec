<!--  NOTE: Auto-generated from the JSON PURL type definition.
Do not manually edit this file. Edit the JSON type definition instead. -->

# PURL Type Definition: deb

- **Type Name:** Debian package
- **Description:** Debian packages, Debian derivatives, and Ubuntu packages
- **Schema ID:** `https://packageurl.org/types/deb-definition.json`

## PURL Syntax

The structure of a PURL for this package type is:

    pkg:deb/<namespace>/<name>@<version>?<qualifiers>#<subpath>

## Repository Information

- **Use Repository:** Yes
- **Note:** There is no default package repository, this should be implied either from the distro qualifiers key or using a base url as a repository_url qualifiers key.

## Namespace definition

- **Requirement:** Required
- **Native Label:** vendor
- **Note:** `The namespace is the "vendor" name such as "debian" or "ubuntu". It is not case sensitive and must be lowercased.`

## Name definition

- **Native Label:** name
- **Note:** `The name is not case sensitive and must be lowercased.`

## Version definition

- **Native Label:** version
- **Note:** `The version is the version of the binary (or source) package.`

## Qualifiers Definition

| Key  | Requirement | Native name | Default Value | Description |
|------|-------------|-------------|---------------|-------------|
| arch | Optional |  |  | arch is the qualifiers key for a package architecture. The special value arch=source identifies a Debian source package that usually consists of a Debian Source control file (.dsc) and corresponding upstream and Debian sources. The dpkg-query command can print the name and version of the corresponding source package of a binary package, e.g. dpkg-query -f ${source:Package} ${source:Version} -W <binary package name> |

## Examples

- `pkg:deb/debian/curl@7.50.3-1?arch=i386&distro=jessie`
- `pkg:deb/debian/dpkg@1.19.0.4?arch=amd64&distro=stretch`
- `pkg:deb/ubuntu/dpkg@1.19.0.4?arch=amd64`
- `pkg:deb/debian/attr@1:2.4.47-2?arch=source`
- `pkg:deb/debian/attr@1:2.4.47-2%2Bb1?arch=amd64`
