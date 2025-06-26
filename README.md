# educup-scripts-runner

Public repository that holds GitHub Actions workflows to execute CSV processing tasks defined in `educup/educup-scripts`.

## Available workflows

* **process-csv-redis-external.yml** – reusable composite action that clones `educup/educup-scripts` and runs the CLI to push data to Upstash Redis.
* **public-tx-pc-redis.yml** – example dispatcher to process `TX PC 2025.csv`.
* **public-tx-lh-redis.yml** – example dispatcher to process `TX LH 2025.csv`.

## Usage

1. Fork or reuse this repository (or copy the workflow files to your own).
2. Set the following repository secrets:
   * `UPSTASH_REDIS_REST_URL`
   * `UPSTASH_REDIS_REST_TOKEN`
   * Optional `GH_PAT` if `educup/educup-scripts` is private.

3. Trigger the desired workflow via "Run workflow" button or via the GitHub API.

## Configuration

The workflows are configured to process CSV files from the `educup/educup-scripts` repository. The CSV paths are relative to that repository's root directory.
