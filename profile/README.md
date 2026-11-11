## Morrowdock

**Kinematically checked 3D mechanism explainers.** An AI model writes a gear train, a slider-crank or an engine
cutaway as JSON. The MartyGraphics engine solves the motion, refuses a wrong model with an exact reason, and renders
the stills and the video. It checks motion and layout. It does not check whether the words are true.

<p align="center">
  <a href="https://github.com/morrowdock/martygraphics"><img src="https://raw.githubusercontent.com/morrowdock/martygraphics/933db57c6beb9863f543c4519d35ece84952ebb3/docs/assets/turbofan/labelled.png" width="720" alt="Labelled cutaway of a schematic two-spool turbofan rendered by MartyGraphics: fan, compressors, combustor, turbines and the HP shaft in orange."></a>
</p>

A schematic turbofan from 38 lines of example JSON, written directly in the format (not a prompt run). From a prompt, Claude Haiku 5.5 wrote a robot-joint
gearbox: the engine refused it once (`constraint.gearMesh.phase`: 20 + 56 teeth do not divide by 3 equally spaced planets), and
the model's repair was accepted.

| Repository | What it is |
| --- | --- |
| [martygraphics](https://github.com/morrowdock/martygraphics) | The Swift engine: solid 3D kernel, gear and joint solver, strict check, renderer, `marty-solid` tool |
| [marty](https://github.com/morrowdock/marty) | An AI teacher on the engine (early preview): an MCP server and a research, plan, write, check, repair loop |
| [marty-model](https://github.com/morrowdock/marty-model) | The plan and data pipeline for a small open model that writes checked scenes (no weights yet) |

**Honest status.** Early preview; APIs and formats can change. Apple platforms only (macOS 14+, iOS 17+). In a
50-question development test, Claude Haiku 5.5 got all 40 in-scope questions accepted within three repairs, but only 29 of 40 were
fully correct in mechanics. AI agents (mainly Claude Opus 5.5) wrote the code under the direction of Collin Craig,
with independent reviews by other AI models. The published fact checks are AI model checks, not an engineer's review.

Code: Apache-2.0. The Morrowdock and Marty names and logos are not licensed. ·
[morrowdock.app](https://morrowdock.app) · [hello@morrowdock.app](mailto:hello@morrowdock.app)
