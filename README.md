## ⛓️ Chainsaw
[![Tests](https://github.com/codebysushil/chainsaw/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/codebysushil/chainsaw/actions/workflows/tests.yml)

Chainsaw ⛓️

## Setup and Code Execute
Full CI code snippet. if want use Docker' Container than used 
```yml
container:
image:hhvm/hhvm:latest
```
or if want to use `Setup Hacklang` go with

```yml
- name: Setup Hacklang
  uses: CodeWithSushil/setup-hacklang@v2.2
```

Here Full code with **Docker' container** and **Setup Hacklang**.

```yml
name: Tests

on: [push]                                            
jobs:
  tests:
    runs-on: ubuntu-latest

    container:
      image: hhvm/hhvm:latest

    steps:

      - name: Checkout
        uses: actions/checkout@v5

        # - name: Setup Hacklang
        # uses: CodeWithSushil/setup-hhvm@v2.2

      - name: Running hack script
        run: hhvm -c hhvm.ini src/index.php

```
