<!--
SPDX-FileCopyrightText: 2021-2024 Robin Vobruba <hoijui.quaero@gmail.com>

SPDX-License-Identifier: CC0-1.0
-->

# OKH RDF triple-store tester

---
---

!!!
**DEPRECATED**
This repo is now deprecated,
and superseded by <https://github.com/osegermany/OKH-RDF-DB>.
!!!

---
---

<s>

[![License](
    https://img.shields.io/github/license/OPEN-NEXT/LOSH-RDF-DB-tester.svg?style=flat)](
    ./LICENSE.txt)
[![REUSE status](
    https://api.reuse.software/badge/github.com/OPEN-NEXT/LOSH-RDF-DB-tester)](
    https://api.reuse.software/info/github.com/OPEN-NEXT/LOSH-RDF-DB-tester)

This contains instructions and scripts
to help you easily test the [OKH](https://github.com/iop-alliance/OpenKnowHow)
[data](https://gitlab.opensourceecology.de/verein/projekte/losh-rdf)
with the [Apache Jena](https://jena.apache.org/) triple-store.

In short, it:

1. (backend & frontend) Downloads the required software (to `~/.local/opt/apache-jena-*`)
2. (backend) Creates a directory (`./build/rdf_db/`) to use as the triple-store
3. (backend) Loads the OKH ontology and all the crawled hardware projects
    into the triple-store
4. (frontend, _optional_) Starts a local web-interface
    that allows you to run SPARQL queries on the data

## Usage

```bash
# Gets this project onto your computer.
git clone "https://github.com/OPEN-NEXT/LOSH-RDF-DB-tester.git" "OKH-DB-tester"
cd "OKH-DB-tester"

# Creates the DB and fills it with the data
# (See the output for instructions
# of how to run SPARQL queries on the command-line).
# NOTE This might take quite a while to finish
run/fill-db

# Starts the web-interface
# (see the output for the URL
# you will have to open in your browser)
run/web-ui
```

The web-UI will then (probably) be available at:

<http://localhost:3030/#/dataset/okh/query>

You can now try your first [sample query](res/sample-query.txt)
on the OKH data.

</s>
