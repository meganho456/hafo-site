# Hafo Sync Agent — Architecture Spec

## What it is
Lightweight background service that bridges the clinic's existing PMS with the Hafo / Google Cloud platform.

## Implementation
- Language: Python or C# .NET 8
- Deployment: runs on-premise inside the clinic network, no cloud VM required

## Data flow
1. Reads operational data from the clinic PMS via its native interface
2. Anonymises all PII locally — nothing identifiable ever leaves the clinic
3. Publishes anonymised events to **Google Cloud Pub/Sub**
4. All AI processing runs on GCP: **Vertex AI**, **MedLM**, **BigQuery**, **Cloud Run**
5. Results (schedules, alerts, analytics) are written back into the clinic's existing PMS via its native API

## Key constraint
**Raw patient data NEVER leaves the clinic premise.** This is both a PDPA (Singapore) and HIPAA (US) requirement and a core sales promise.

## On-page copy to use
- "The Hafo Sync Agent — a lightweight Python / C# .NET 8 background service — connects to your existing PMS via native API."
- "It anonymises PII locally before any data reaches Google Cloud, then writes results back automatically."
- "Raw patient data never leaves your clinic."
