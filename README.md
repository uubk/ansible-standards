# Ansible-standards
A repository containing my [ansible-review](https://github.com/willthames/ansible-review).
At the moment, this is mostly the default config.

## Usage
To use this with e.g. CircleCI, just use the following configuration:
```
version: 2.0
jobs:
  build:
    docker:
      - image: uubk/ansible-standards:latest
    steps:
      - checkout
      - run: ansible-lint .
      - run: git ls-files | xargs ansible-review
```

## License
MIT
