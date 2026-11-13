# The Spatial Harness / ReVSI evidence walkthrough demo

[Open the interactive demo](https://spatial-harness-demo.github.io/)

Six selected correct examples, grouped by category:

| Category | Cases |
| --- | --- |
| Counting | **214 — Count backpacks** |
| Distance | **2225 — Object distance**, **3457 — Closest object** |
| Direction | **5372 — Direction · backward**, **5293 — TV direction** |
| Area | **6713 — Combined area** |

Cases **214** and **5293** show the recorded initial attempt, executed replan and correct final answer. Case 214 reacquires backpack evidence after a failed SAM call and returns **1**. Case 5293 reuses evidence, changes the TV pair decision from **Keep separate** to **Merge**, and returns **A — left**. Neither activates a backup or rewrites the grounding prompt.

Use the top arrows to step through tool results and verifier checks, or Play to animate each round. Playback pauses between rounds. Repeated checks are grouped in expandable summaries, with every original decision and evidence image available. Scene videos run at 4× speed. This static walkthrough does not launch inference.

Ground truth and per-case accuracy remain visible. The original 13-case aggregate metrics in About retain their historical denominator; they are not scores for these six selected examples or the later 39-question and B200 runs.

## Site files and deployment

The complete static site, including HTML, CSS, JavaScript, data and media, is **site.zip** in [release v1.1.0](https://github.com/spatial-harness-demo/spatial-harness-demo.github.io/releases/tag/v1.1.0). The release also includes SHA256SUMS.

The manually triggered Pages workflow downloads this exact release archive, verifies its SHA-256 and deploys it using GitHub’s official Pages actions. Version 1.0.0 remains available for rollback. No inference endpoint, analytics or external runtime service is required.

For local viewing, unzip site.zip, run `python3 -m http.server 8000` in the extracted folder, and open the server address.

Source provenance and media hashes are included in the data files. The two B200 recordings predate the later SAM3 argument fix; expired contact sheets restored from their recorded layouts are labeled. This demo does not grant new rights to third-party ReVSI scene content or imply that these selected cases represent full-benchmark performance.
