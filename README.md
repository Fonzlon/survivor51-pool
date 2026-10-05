# Survivor 51 Pool

Fantasy pool scoreboard for Odiya, Yohai, Adam and Lonnie.
Live at https://fonzlon.github.io/survivor51-pool/

## Scoring
A picked contestant voted out Nth earns each player who picked them N points.
The Sole Survivor (last one standing) earns 21.

## How state works
The elimination order lives in `docs/state.json`. Everyone reads it from the
Pages site (auto-refresh every 30s). The scorekeeper clicks **🔑 Scorekeeper
login** in the footer and pastes a GitHub fine-grained token scoped to this
repo only with **Contents: Read and write**; Eliminate / Undo / Reset then
commit `state.json` directly via the contents API. The token is stored only
in that browser's localStorage.

Create a token: https://github.com/settings/personal-access-tokens/new
