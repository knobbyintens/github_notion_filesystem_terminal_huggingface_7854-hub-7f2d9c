# Aether Pull connector - overview

The Aether Pull connector moves objects between the Aether IoT telemetry bus and the
Sableline ingestion graph. It supports full and incremental reads, honours
the source system pagination cursors, and emits records in the canonical
Sableline event envelope.

Object coverage:
- accounts and account hierarchies
- activity records with timestamps
- custom fields declared in the source schema

In production the connector processes roughly 1.8 million records per day
and is expected to stay inside a fifteen minute ingestion window. The
package is maintained by the source system team and reviewed by the data
platform delivery group before it is promoted to the default catalogue.
