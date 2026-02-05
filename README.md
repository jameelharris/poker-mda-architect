# Problem Statement

Live poker, unlike its online counterpart, lacks a commercial dataset derived from pre-recorded or live broadcasts. While online play is natively structured and machine-readable, live broadcast data remains trapped in unstructured video formats, creating a massive "dark data" gap in the industry.

The absence of these datasets has led to several systemic failures:

* Sector Stagnation: Domains such as game hosting, professional coaching, and sports journalism—which serve as primary growth channels for the game—have seen their efficiency stagnate or regress over the past two decades due to a reliance on manual data entry and anecdotal analysis.

* Failed Interdependence: There is a total lack of interoperability between media production and data-driven utility. Without a shared data layer, the industry cannot sustain logical growth pipelines—such as casinos identifying struggling players for coaching referrals, or journalists using verified win-rate improvements to craft compelling "player journey" narratives. This disconnect prevents the poker industry from leveraging the interdependent ecosystems common in other professional sports.

* Market Share Erosion: In the hyper-competitive landscape of the attention economy, poker is in a state of managed decline. It currently possesses no strategic mechanism to operationalize its most valuable content into the structured datasets required to scale its market share and engage a data-literate audience.

## Business Context
<p align="center">
  <img src="docs/business-arch.svg" width="1000" alt="Business Architecture Diagram">
</p>

[View Full Diagram](https://s.icepanel.io/dLY1ttD4YFdhq8/JUWB)

## System Architecture
<p align="center">
  <img src="docs/system-arch.svg" width="1000" alt="System Architecture Diagram">
</p>

[View Full Diagram](https://s.icepanel.io/dLY1ttD4YFdhq8/fsjK)

## Data Model
<img src="docs/poker-erd.drawio.svg" width="100%" alt="Poker Data Architecture ERD">

[View Full Diagram](./docs/poker-erd.drawio.svg)

## Tech Stack
The following technologies are utilized in the Hand History Hub:

### Systems/Platforms
*   **GCP:** Google Cloud Platform, the primary cloud provider for the system.

### Applications/Services
*   **Cloud Run:** Serverless platform for running containerized applications, used by the Downloader and Video Clipper.
*   **Dataform:** Service for data transformation within the AI-enabled Data Transformation component.
*   **Gemini (AI) & BQML:** Utilized in the AI-enabled Data Transformation for decomposing and translating clips.
*   **Eventarc:** Event management service, used by the Video Clipper Trigger.
*   **Scheduler:** Implied for scheduling download jobs (e.g., every 30 minutes) by the Downloader Trigger.

### Data Stores
*   **Cloud Storage:** Used for storing Video Assets and Clip Assets.
*   **BigQuery:** Our scalable and serverless data warehouse, used for Poker Broadcast Registry and Hand History.

## How to Run
[//]: # (TODO: Add detailed instructions on how to set up and run the project)