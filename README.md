# The Spatial Harness / ReVSI evidence walkthrough demo

Explore the recorded plans, tool results and verification evidence at https://spatial-harness-demo.github.io/.

| Category | Case IDs |
| --- | --- |
| Counting | 214, 19, 756 |
| Object size | 1113, 2100, 1187 |
| Object distance | 2225, 2339, 3356 |
| Closest object | 3457, 4036, 4242 |
| Farthest object | 4258, 4416, 4310 |
| Relative direction | 5372, 5293, 5591 |
| Room area | 6713, 6772, 6788 |
| Requested cases | 11, 6382, 6232 |

The seven benchmark categories each contain three full-credit results. Cases 214 and 5293 reached the correct answer after an executed replan.
The requested cases are separate: #11 has a dataset reference but no completed run; #6382 and #6232 have recorded v9 retry 1 attempts that ended with insufficient evidence. Their recovery proposals were not executed.

The original 13-question replay metrics in About retain their original denominator. Per-case numerical scores use MRA; full credit is within 5% relative error.

Play animates recorded events and pauses between rounds. The top arrows move through plans, evidence and verifier decisions. Scene videos use the 64 ordered source frames.

Source records and media hashes are documented in data/category-provenance.json and the other provenance files under data/. The public package excludes private execution logs. No inference service is required.

## Site files and deployment

The complete static site, including HTML, CSS, JavaScript, data and media, is **site.zip** in [release v1.2.0](https://github.com/spatial-harness-demo/spatial-harness-demo.github.io/releases/tag/v1.2.0). The release also includes SHA256SUMS.

The manually triggered Pages workflow downloads this exact release archive, verifies its SHA-256 and deploys it using GitHub’s official Pages actions. Earlier releases remain available for rollback. No inference endpoint, analytics or external runtime service is required.

For local viewing, unzip site.zip, run `python3 -m http.server 8000` in the extracted folder, and open the server address.

Source provenance and media hashes are included in the data files. The two B200 recordings predate the later SAM3 argument fix; expired contact sheets restored from their recorded layouts are labeled. This demo does not grant new rights to third-party ReVSI scene content or imply that these selected cases represent full-benchmark performance.
