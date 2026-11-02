# bdlglua.github.io

The public [BDLMiner V2 website and USB installer](https://bdlglua.github.io/)
is published at the account's root address. The original BDLXS / NovaFlow
template is preserved at [bdlglua.github.io/bdlxs/](https://bdlglua.github.io/bdlxs/).

The site includes guided installation/update paths, a measured hardware
comparison, offline interactive miner/fleet demos, troubleshooting, release
highlights, a community-photo submission path and the owner's GitHub Sponsors
link. Public content and reviewed photos are maintained in
[`installer/content.json`](https://github.com/bdlglua/BDLMinerV2/blob/main/installer/content.json);
see the [website maintenance guide](https://github.com/bdlglua/BDLMinerV2/blob/main/installer/README.md).

## Publishing

The **Publish BDLMiner** workflow builds the website using the current `main`
branch and published releases of [BDLMinerV2](https://github.com/bdlglua/BDLMinerV2).
It uses that project's existing channel builder, so the default installer stays
on the latest stable release and `/beta/` remains opt-in. Factory images and
installer manifests are hosted on this site alongside the page.

The workflow runs on every push here, once an hour, or manually from the
Actions tab. It publishes the generated files using GitHub Pages Actions;
generated firmware binaries are not committed to this repository.

It waits for an existing branch-based Pages build to finish before deploying
the generated site, then checks the live installers, discovery data, demo files
and the preserved BDLXS page.

The existing project website at `/BDLMinerV2/` remains published separately.
Existing firmware update links continue to use it.

`index.html` is a fallback link to the project website for the initial migration
from branch-based Pages. The Actions deployment replaces it with the full site.
The original template's files and customization notes are in `bdlxs/`.
