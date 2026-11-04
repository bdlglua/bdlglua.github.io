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

The home page is a short overview. Each section has its own page with shared
navigation, in both English and French:

- [Flash / Flasher](https://bdlglua.github.io/flash.html)
- [Get started](https://bdlglua.github.io/start.html)
- [Supported boards](https://bdlglua.github.io/boards.html)
- [Interactive demos](https://bdlglua.github.io/demo.html)
- [Troubleshooting](https://bdlglua.github.io/faq.html)
- [Releases](https://bdlglua.github.io/releases.html)
- [Live statistics](https://bdlglua.github.io/stats.html)
- [Community](https://bdlglua.github.io/gallery.html)
- [Support BDLMiner](https://bdlglua.github.io/support.html)

The same pages are available under `/beta/`. Previous home-page fragment links
continue to open the appropriate page. Selecting a board in the comparison
passes its profile to the USB flasher.

The statistics page also groups miner counts and combined hashrate by public
pool. From firmware 2.0.3, **Share my pool anonymously** is enabled by default
and can be disabled in Network settings; saved opt-outs are kept. Public pools
link to their official website, with the URL shown below the name. Private/custom endpoints are grouped
as **Other / private pool** before leaving the device. Older reports, disabled
pool sharing and disconnected pools appear as **Not shared**.

From firmware 2.1.0, the miner can select BTC or BCH (SHA-256d). The
[configuration guide](https://github.com/bdlglua/BDLMinerV2/blob/main/docs/mining-coins.md)
explains matching pools, addresses/accounts and BCH Stratum V1. Live statistics
show a separate cryptocurrency breakdown in a table that fills the card, with
aligned numeric columns; old reports without a ticker count under BTC. The dashboard and hub demos use the same selection controls.

From 2.1.1, **User agent** is one dropdown: `NerdMinerV2` or
`BDLMinerV2/2.1.1`. There are no Automatic/Manual modes or custom text entry.
The native identity follows the installed firmware version, while a selected
NerdMinerV2 identity is retained. The setup portal and interactive demo use the
same choices.

From 2.2.0, the SHA-256d selector adds **BSV**, **eCash (XEC)** and
**DigiByte SHA-256d (DGB)** alongside BTC/BCH. The new profiles use Stratum V1,
matching pool/address settings and separate public totals. DGB rejects jobs from
its other mining algorithms. The FAQ and coin guide explain pool requirements;
physical measurements on these new pools remain pending.

From 2.3.0, [My miners](https://bdlminer-stats.bdlminer-bot.workers.dev/remote)
provides opt-in private remote readings and seven-day history, without a local
hub. Pair boards with a browser-generated access key; anonymous public totals
remain separate. The private viewer uses its own isolated scripts and supports
permanent key revocation. See the [setup and privacy guide](https://github.com/bdlglua/BDLMinerV2/blob/main/docs/remote-access.md).

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
the generated site, then checks all ten pages in both channels, discovery data,
demo files, pool statistics markup, installer manifests and the preserved BDLXS page.

The existing project website at `/BDLMinerV2/` remains published separately.
Existing firmware update links continue to use it.

`index.html` is a fallback link to the project website for the initial migration
from branch-based Pages. The Actions deployment replaces it with the full site.
The original template's files and customization notes are in `bdlxs/`.
