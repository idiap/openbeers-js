<!--
SPDX-FileCopyrightText: Copyright © 2024-2025 Idiap Research Institute <contact@idiap.ch>
SPDX-FileContributor: David Geissbühler <david.geissbuhler@idiap.ch>
SPDX-License-Identifier: Apache-2.0
-->

# Generate/update the library from OpenAPI specs

1. Download the OpenAPI JSON spec file ```.generate/openapi.json``` and replace the existing version in the root of this package

2. Install OpenJDK (MacOS) 

```sh
brew install openjdk
sudo ln -sfn /opt/homebrew/opt/openjdk/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk.jdk
```

3. Install ```openapi-generator-cli```

```sh
npm install @openapitools/openapi-generator-cli -g
```

4. Generate package

```sh
openapi-generator-cli generate -i .generate/openapi.json -g typescript-fetch -c .generate/config.yml  
```
