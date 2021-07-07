The Search Share extension is based on the PageSigner project by TLS Notary: https://github.com/tlsnotary

## Thank you
Please accept my massive thank you for trying out this app!  I really appreciate any time you spend on it. 

# Before using, please read!

Explainer / Blog post: https://github.com/rjaus/search-share-docs/blob/master/README.md
How to use: https://github.com/rjaus/search-share-docs/blob/master/How-to-submit.md

# How to Install this extension

## Requirement:
This extension relys upon the PageSigner companion extension, you will be prompted to install it when attempting to use SearchShare.  The companion extension can be found here: https://chrome.google.com/webstore/detail/pagesigner-helper-app/oclohfdjoojomkfddjclanpogcnjhemd

Search Share works with **Chromium-based browsers** (e.g. Chromium, Vivaldi, Brave, Google Chrome)

## Install Instructions:

1. Clone or download (and extract) the [Search Share extension](https://github.com/rjaus/search-share-extension).

- Clone: `clone https://github.com/rjaus/search-share-extension.git`
- Download: https://github.com/rjaus/search-share-extension/archive/refs/heads/master.zip 

2. Open Chromium

3. Go to chrome://extensions/ and enable "Developer Mode" (top right hand corner)

4. Click "Load Unpacked"

5. Select the directory where you cloned / extracted the extension

6. Now install the PageSigner Companion app (Chrome App): https://chrome.google.com/webstore/detail/pagesigner-helper-app/oclohfdjoojomkfddjclanpogcnjhemd



## Features:
This extension is a modified version of the PageSigner extension by TLS Notary.  It has most of the existing features plus a few more to aid the specific use case of sharing search results.

- upon generating a proof, the proof is immediately uploaded to the Search Share API, for the purpose of sharing publicly.
- The proof is generated for the relevant page/request dependant on the search engine used.  This is only relevant to DDG, which retrieves the search results via a JS request

## Permissions:
The extension requests '<all_urls>' permissions which is overkill for it's needs.  If you're uncomfortable with that, replace '<all_urls>' with the following. Replace the google url with your desired country edition as required.

"https://*.duckduckgo.com/*",

"https://search.brave.com/*",

"https://bing.com/*",

"https://google.com/*"

Untested, but it should work.  Check the console logs for permission errors, you may need to play with the wildcards. (note: you should be watching the console.logs of background.html, accessed via the chromium extensions settings page)