# actions-poetry

GitHub Actions for Python projects using poetry with cache

[![license](https://img.shields.io/github/license/enkeys/actions-poetry.svg)](https://github.com/enkeys/actions-poetry/blob/main/LICENSE)
[![release](https://img.shields.io/github/release/enkeys/actions-poetry.svg)](https://github.com/enkeys/actions-poetry/releases/latest)
[![GitHub release date](https://img.shields.io/github/release-date/enkeys/actions-poetry.svg)](https://github.com/enkeys/actions-poetry/releases)

- [python-poetry/poetry: Python dependency management and packaging made easy.](https://github.com/python-poetry/poetry)

## Getting started

### Create your workflow

```yaml
name: CI
on: pull_request

jobs:
  ci:
    strategy:
      fail-fast: false
      matrix:
        python-version: [ 3.9 ]
        os: [ ubuntu-latest ]
    runs-on: ${{ matrix.os }}
    steps:
      - uses: actions/checkout@v2
          -
      - uses: actions/setup-python@v2
        with:
          python-version: ${{ matrix.python-version }}

      - name: Install poetry
        uses: enkeys/actions-poetry@v1.0.0

      - name: View poetry --help
        run: poetry --help
```

## License

[MIT License - enkeys/actions-poetry]

[MIT License - abatilo/actions-poetry (Original author)]: https://github.com/abatilo/actions-poetry/blob/master/LICENSE

[MIT License - enkeys/actions-poetry]: https://github.com/enkeys/actions-poetry/blob/main/LICENSE