# Delta Sync connector - usage

## Setup
1. Set SABLELINE_API_URL and SABLELINE_API_TOKEN in the runtime environment.
2. Install the package with `pip install -e .` from the delta-sync folder.
3. Run a small backfill first: `python -m connector --limit 100`.

## Configuration
The connector reads `manifest.json` when present and otherwise falls back to
the platform defaults. Set the schedule through the deployment descriptor
rather than editing the package.

## Example
```
python -m connector --source delta-sync --since 2026-09-01 --until 2026-09-30
```

Check the run summary for the number of written, skipped and rejected
records. Rejected records are written to the dead letter stream with the
source identifier attached so they can be replayed after a fix.
