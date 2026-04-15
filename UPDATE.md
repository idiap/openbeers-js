<!--
SPDX-FileCopyrightText: Copyright © 2024-2025 Idiap Research Institute <contact@idiap.ch>
SPDX-FileContributor: David Geissbühler <david.geissbuhler@idiap.ch>
SPDX-License-Identifier: Apache-2.0
-->

# openbeers-py

OpenBEERS API Python client

# Installation Dev

```sh
npm install
npm run build
```

Then install a JVM (Java). 

On MacOS:

```sh
brew install openjdk
brew info openjdk
```

Then export PATH as instructed

# (Re)Generate API

Install ```openapi-generator-cli``` globally via npm (see openbeers-js) and a JVM.

```sh
openapi-generator-cli generate -i .generator/openapi.json -g typescript-fetch -c .generator/config.yml
```
