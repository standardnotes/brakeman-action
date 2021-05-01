# brakeman-action

This action runs [Brakeman](https://brakemanscanner.org/) against a repository's source code to find security vulnerabilities.

> Brakeman is a free vulnerability scanner specifically designed for Ruby on Rails applications. It statically analyzes Rails application code to find security issues at any stage of development.

## Usage

```yaml
name: Test pull requests
on:
  pull_request:
    branches: [ main, develop ]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - name: Brakeman action
        uses: standardnotes/brakeman-action@v1.0.0
        with:
          options: "--color -q"
```

## License

This project is released under the [MIT License](LICENSE).
