# bdlglua.github.io

The public [BDLMiner V2 website and USB installer](https://bdlglua.github.io/)
is published at the account's root address. The original BDLXS / NovaFlow
template is preserved at [bdlglua.github.io/bdlxs/](https://bdlglua.github.io/bdlxs/).

## Publishing

The **Publish BDLMiner** workflow builds the website using the current `main`
branch and published releases of [BDLMinerV2](https://github.com/bdlglua/BDLMinerV2).
It uses that project's existing channel builder, so the default installer stays
on the latest stable release and `/beta/` remains opt-in. Factory images and
installer manifests are hosted on this site alongside the page.

The workflow runs on relevant changes here, once an hour, or manually from the
Actions tab. It publishes the generated files using GitHub Pages Actions;
generated firmware binaries are not committed to this repository.

The existing project website at `/BDLMinerV2/` remains published separately.
Existing firmware update links continue to use it.

`index.html` is a fallback link to the project website for the initial migration
from branch-based Pages. The Actions deployment replaces it with the full site.
The original template's files and customization notes are in `bdlxs/`.
