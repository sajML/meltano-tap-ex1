# dummyjson tap-ex1 

`tap-ex1` is a Singer tap for dummyjson.com (It is a exercise :)

Built with the [Meltano Tap SDK](https://sdk.meltano.com) for Singer Taps.

<!--

Developer TODO: Update the below as needed to correctly describe the install procedure. For instance, if you do not have a PyPi repo, or if you want users to directly install from your git repo, you can modify this step as appropriate.

## Installation

Install from PyPi:

```bash
pipx install tap-ex1
```

Install from GitHub:

```bash
pipx install git+https://github.com/ORG_NAME/tap-ex1.git@main
```

-->

## Configuration

### Accepted Config Options

<!--
Developer TODO: Provide a list of config options accepted by the tap.

This section can be created by copy-pasting the CLI output from:

```
tap-ex1 --about --format=markdown
```
-->

A full list of supported settings and capabilities for this
tap is available by running:

```bash
tap-ex1 --about
```

### Configure using environment variables

This Singer tap will automatically import any environment variables within the working directory's
`.env` if the `--config=ENV` is provided, such that config values will be considered if a matching
environment variable is set either in the terminal context or in the `.env` file.

### Source Authentication and Authorization

<!--
Developer TODO: If your tap requires special access on the source system, or any special authentication requirements, provide those here.
-->

## Usage

You can easily run `tap-ex1` by itself or in a pipeline using [Meltano](https://meltano.com/).

### Executing the Tap Directly

```bash
tap-ex1 --version
tap-ex1 --help
tap-ex1 --config CONFIG --discover > ./catalog.json
```

## Developer Resources

Follow these instructions to contribute to this project.

### Initialize your Development Environment

```bash
pipx install poetry
poetry install
```

### Create and Run Tests

Create tests within the `tests` subfolder and
  then run:

```bash
poetry run pytest
```

You can also test the `tap-ex1` CLI interface directly using `poetry run`:

```bash
poetry run tap-ex1 --help
```

### Testing with [Meltano](https://www.meltano.com)

_**Note:** This tap will work in any Singer environment and does not require Meltano.
Examples here are for convenience and to streamline end-to-end orchestration scenarios._

<!--
Developer TODO:
Your project comes with a custom `meltano.yml` project file already created. Open the `meltano.yml` and follow any "TODO" items listed in
the file.
-->

Next, install Meltano (if you haven't already) and any needed plugins:

```bash
# Install meltano
pipx install meltano
# Initialize meltano within this directory
cd tap-ex1
meltano install
```

Now you can test and orchestrate using Meltano:

```bash
# Test invocation:
meltano invoke tap-ex1 --version
# OR run a test `elt` pipeline:
meltano elt tap-ex1 target-jsonl
```

### SDK Dev Guide

See the [dev guide](https://sdk.meltano.com/en/latest/dev_guide.html) for more instructions on how to use the SDK to
develop your own taps and targets.

###

docker build -t ex1-tap-img -f Dockerfile.meltano .
docker run --volume $(pwd)/output:/app/output ex1-tap-img
docker run --volume $(pwd)/output:/app/output ex1-tap-img run tap-ex1 target-csv


docker build -t ex1-fastapi-img -f Dockerfile.fastapi .
docker run -p 8001:8000 ex1-fastapi-img
docker run -p 8001:8000 ex1-fastapi-img uvicorn run_api:app --host 0.0.0.0 --port 8000


docker run astro_067921/airflow:latest ls

docker run --volume $(pwd)/output:/app/output sajjadgoudarzi/vicev-ex1-meltano:latest