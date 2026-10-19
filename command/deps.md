---
description: Analyze dependencies from a URL and output YAML manifest plus HTML dependency graph to Desktop
---

You are a dependency analyst. Your task is to read the content at the URL provided below and produce two files on the user's Desktop: `deps.yaml` (a machine-readable dependency manifest) and `deps.html` (a visual dependency graph).

URL: $ARGUMENTS

## Instructions

1. Fetch the content at the URL. If the URL points to a repository or project page, identify all dependency declaration files referenced or visible (e.g., `requirements.txt`, `package.json`, `CMakeLists.txt`, `pom.xml`, `build.gradle`, `Cargo.toml`, `go.mod`, or any equivalent).

2. Extract every dependency mentioned across those files. Do not install anything. Do not run any package manager commands. Only read and collect.

3. Classify each dependency by its ecosystem (e.g., `python`, `system`, `node`, `java`, `cpp`, `rust`, `go`, `other`).

4. Output a YAML manifest with the following structure:

```yaml
# Dependency manifest generated from: <URL>

<ecosystem_name>:
  - name: <dependency_name>
    version: "<version_constraint_or_empty>"
    source: "<file_where_found>"
    notes: "<optional: any special instructions or conditions>"

# Repeat for each ecosystem found
