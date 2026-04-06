# Design Brief: Data Engineering for Spatial Systems

## What this book is

A book for engineers who need to build systems that move, store, transform, and serve spatial data at scale. Not a framework guide. Not a cloud vendor tutorial. The book earns the reader's trust by showing working systems — minimal, correct, and instructive — and then explaining why they are designed the way they are.

## What it is not

- Not a GIS manual (assumes familiarity with spatial data concepts from Computational Geography)
- Not a cloud vendor guide (uses open-source tooling throughout)
- Not an academic treatment of database theory (pragmatic first, theory when it earns its place)
- Not a catalogue of tools (fewer tools, understood deeply)

## Core design principle

Every chapter builds toward a thing that works. A working PostGIS query. A running pipeline. A deployed API. The theory exists to explain the working thing, not to precede it.

## The lab thread

Each chapter closes with a "build this" section: a minimal implementation of the chapter's central concept, specified well enough to run. By the end of Ch 8, the eight components together form a simple but real spatial data platform — one that ingests a satellite data source, transforms it, stores it in a spatial database, exposes it via an API, and serves predictions from a trained model.

The reader who completes all eight "build this" sections has built something. That is the point.

## Voice

Practical, dry, technically precise. Like a senior engineer explaining to a junior engineer why something is done the way it is — not lecturing, just thinking aloud. No unnecessary hedging. No "it depends" without specifying what it depends on.

## Tooling choices

All tools are open-source. Where commercial cloud services are relevant, open-source alternatives are always shown first.

| Domain | Primary tools |
|--------|--------------|
| Spatial data formats | GDAL, GeoJSON, GeoParquet, cloud-optimised GeoTIFF |
| Spatial databases | PostgreSQL + PostGIS, DuckDB with spatial extension |
| Data transformation | dbt, Pandas, GeoPandas |
| Pipeline orchestration | Prefect (simpler) or Airflow (battle-tested) |
| Data quality | Great Expectations, dbt tests |
| Cloud storage | MinIO (local S3-compatible), S3-compatible patterns |
| Streaming | Kafka (full) or MQTT (sensor-scale) |
| APIs | FastAPI + GeoAlchemy2, OGC API standards |
| ML platform | MLflow (experiment tracking), Feast (feature store) |

## Repeating visual threads

1. **Architecture diagrams** — data flow diagrams showing source → transform → load → serve. Consistent notation across all chapters.

2. **Query execution plans** — EXPLAIN ANALYZE output visualised. Teaches readers to read what the database is actually doing.

3. **Latency/throughput profiles** — what does this system actually do under load? Real numbers, honest benchmarks.

## Cross-links to other WH books

- **← Comp Geo Lab investigations:** The data sources that need engineering pipelines.
- **← Systems Thinking Ch 6 (Data as a System):** The conceptual framing for why pipelines fail in counterintuitive ways.
- **→ Data-AI Ch 6–8:** The ML models that the platforms in Ch 8 serve.

## Status tracking

| Chapter | Status | Notes |
|---------|--------|-------|
| 01-data-architecture | seed | |
| 02-spatial-databases | seed | |
| 03-pipelines-and-etl | seed | |
| 04-cloud-infrastructure | seed | |
| 05-streaming-and-realtime | seed | |
| 06-apis-and-access-patterns | seed | |
| 07-data-quality-and-governance | seed | |
| 08-platform-architecture-for-ml | seed | |
