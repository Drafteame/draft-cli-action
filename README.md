# Draft CLI action

Draft is a CLI tool to help you create and manage AWS Lambda functions and services in a monorepo structure.
It provides commands to create new services and lambdas, as well as to invoke them locally.

## Requirements

- Ubuntu amd64 runners

## Installation

```yaml
steps:
  # ...

  - name: Install draft cli
    uses: Drafteame/draft-cli-action@main
    with:
      access_token: ${{ secrets.ACCESS_TOKEN }}
```

## Usage

### Setup Databases

First locate yourself inside the service folder of the monorepo, the execute next command:

```yaml
steps:
  # ...

  - name: Install draft cli
    uses: Drafteame/draft-cli-action@main
    with:
      access_token: ${{ secrets.ACCESS_TOKEN }}

  - name: Setup local database templates
    run: draft local:setup
```
