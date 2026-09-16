# Modifications to scratch-gui

This repository is a **modified version of
[scratch-gui](https://github.com/scratchfoundation/scratch-gui)** by the Scratch
Foundation, distributed — like the original — under the **GNU Affero General
Public License v3.0 only (AGPL-3.0-only)**. See [`LICENSE`](LICENSE).

This notice is provided in accordance with AGPL-3.0 §5(a): the work carries
prominent notices stating that it has been modified, and the date of any change.

Modifications by **AI Lab for Kids** (copyright © 2026 AI Lab for Kids),
for the AI Lab for Kids K-8 machine learning platform.

## Summary of changes

| Area | Change |
|---|---|
| `src/lib/libraries/extensions/index.jsx` | Added five extension library cards — Face Sensing plus AI Lab Vision, Voice, Text and Numbers — so they appear in the "Choose an Extension" picker. The AI Lab icons are temporarily reused from existing Scratch extensions. |
| `src/lib/libraries/extensions/faceSensing/` | **Ported, not authored.** `faceSensing.png` and `faceSensing-small.svg` copied verbatim from [`scratchfoundation/scratch-editor`](https://github.com/scratchfoundation/scratch-editor), which is AGPL-3.0 like this repo. Copyright remains with the Scratch Foundation. |
| `package.json` | Points `scratch-vm` at the local modified fork (`file:../scratch-vm`); pins `react`/`react-dom` to 16.x. |
| `webpack.config.js` | Re-added the sandboxed `extension-worker` entry point so runtime URL-loaded extensions work without rebuilding the whole GUI bundle. |

No upstream scratch-gui behaviour was altered other than the extension-library
registration above; the changes are additive.

Face Sensing shipped to Scratch in October 2025, after the standalone
scratch-gui repo was archived, so it exists only in the mono-repo. The block
implementation it pairs with lives in the companion scratch-vm fork.

## Corresponding Source

The complete corresponding source for the modified Scratch used by the AI Lab
for Kids platform is available at:

- scratch-gui — <https://github.com/neoTogo/scratch-gui>
- scratch-vm — <https://github.com/neoTogo/scratch-vm>
