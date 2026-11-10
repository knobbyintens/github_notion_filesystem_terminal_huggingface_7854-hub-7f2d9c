# Ember Import - API notes

These notes are optional engineering context for reviewers.

- The upstream endpoint enforces 25 requests per second per key.
- Deleted source objects are soft-deleted and surface as tombstone events.
- Timestamps use the source system clock and are normalised to UTC.
- A retry budget of five attempts is used for transient failures.
