# The Spatial Harness / ReVSI evidence walkthrough demo

[Open the interactive demo](https://spatial-harness-demo.github.io/)

A public walkthrough of four recorded ReVSI cases: **2225 Object distance**, **3457 Closest object**, **5372 Direction · backward**, and **6713 Combined area**. It includes scene videos, plans, visual evidence, verifier decisions, evidence memory, answers, ground truth and per-case evaluation.

Use the top arrows to step through evidence checks, or Play to animate each round. Scene videos run at 4× speed. Playback is a recording and does not launch inference.

The original 13-case aggregate metrics shown in About retain their historical denominator. They are not a score for these four selected examples or the fresh 39-question run.

## Site files and deployment

The complete static site, including HTML, CSS, JavaScript, data and media, is available as **site.zip** in [release v1.0.0](https://github.com/spatial-harness-demo/spatial-harness-demo.github.io/releases/tag/v1.0.0). The release also includes SHA256SUMS.

The manually triggered Pages workflow downloads that exact release archive, checks its SHA-256, and deploys it using GitHub’s official Pages actions. No inference endpoint, analytics or external runtime service is required.

For local viewing, unzip site.zip, run `python3 -m http.server 8000` in the extracted folder, and open the server address.

Source provenance and media hashes are included in the site’s data files. This demo does not grant new rights to third-party ReVSI scene content or imply that these selected cases represent full-benchmark performance.
