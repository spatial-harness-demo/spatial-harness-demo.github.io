# The Spatial Harness / ReVSI evidence walkthrough demo

Explore the recorded plans, tool results and verification evidence at https://spatial-harness-demo.github.io/.

| Category | Case IDs |
| --- | --- |
| Counting | 214, 19, 756 |
| Object size | 1113, 2100, 1187 |
| Object distance | 2225, 2339, 3356 |
| Closest object | 3457, 4036, 4242, 4017 |
| Farthest object | 4258, 4416, 4310, 4592 |
| Relative direction | 5372, 5293, 5591, 5899 |
| Room area | 6713, 6772, 6788 |
| Route planning | 6199, 6203 |
| Requested cases | 11, 6382, 6232, 6195 |

The gallery contains 30 cases from 26 scenes. The eight benchmark categories contain 26 full-credit results. Cases 214, 4017, 4592, 5293, and 5899 reached the correct answer after executing replans.
Cases 6199 and 6203 come from the earlier AutoDL geometry solver. Each walkthrough reconstructs how the solver found four landmarks on the current ReVSI 64-frame subset, reviewed SAM3 masks with Qwen3-VL-8B, lifted them with DA3 depth and selected the 3D centers used for both turns. The original review sheets and landmark ambiguities are shown alongside the recorded decisions.
The requested cases are separate: #11 has a dataset reference but no completed run; #6382 and #6232 have recorded v9 retry 1 attempts that ended with insufficient evidence. Their recovery proposals were not executed. Case #6195 shows the two marked floor-lamp candidates, the verifier’s three replies, and the validation failure in its November v9.2 run.

The original 13-question replay metrics in About retain their original denominator. Per-case numerical scores use MRA; full credit is within 5% relative error.

Play animates recorded events and pauses between rounds. The top arrows move through plans, evidence and verifier decisions. Scene videos use the 64 ordered source frames. Recorded DA3 reconstructions appear in Execution, followed by the verifier decision and reason. The depth images use the same scene and frame labels as semantic checks already shown. Four recordings have no earlier semantic frame at reconstruction time.

Source records and media hashes are documented in data/category-provenance.json and the other provenance files under data/. The public package excludes private execution logs. No inference service is required.

## Site files and deployment

The complete static site, including HTML, CSS, JavaScript, data and media, is **site.zip** in [release v1.6.0](https://github.com/spatial-harness-demo/spatial-harness-demo.github.io/releases/tag/v1.6.0). The release also includes SHA256SUMS.

The manually triggered Pages workflow downloads this exact release archive, verifies its SHA-256 and deploys it using GitHub’s official Pages actions. Earlier releases remain available for rollback. No inference endpoint, analytics or external runtime service is required.

For local viewing, unzip site.zip, run `python3 -m http.server 8000` in the extracted folder, and open the server address.

Source provenance and media hashes are included in the data files. The two B200 recordings predate the later SAM3 argument fix; expired contact sheets restored from their recorded layouts are labeled. This demo does not grant new rights to third-party ReVSI scene content or imply that these selected cases represent full-benchmark performance.
