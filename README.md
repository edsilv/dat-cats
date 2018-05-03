# dat-cats

A [IIIF](http://iiif.io) collection of cats served over [dat](https://datproject.org/)!

Open this url in [Beaker Browser](https://beakerbrowser.com/):

    dat://97fa96d07caba5e4b5c588f7b93b4df85ce936dabfc5262414dec0a16c362b1f


## How-to

First I copied [uv-hello-world](https://github.com/UniversalViewer/uv-hello-world) to create a simple page with the [Universal Viewer](http://universalviewer.io)

I then copied the cats collection folder from https://github.com/edsilv/biiif-workshop into the root of my project.

Then ran:

    npm install dat -g
    npm install biiif-cli --save-dev
    dat create
    dat share

Copied the generated dat link and added a [biiif-cli](https://github.com/edsilv/biiif-cli) `build` script to my package.json `scripts` section using the dat link as the `-u` option:

    "build": "./node_modules/.bin/biiif collection -u dat://97fa96d07caba5e4b5c588f7b93b4df85ce936dabfc5262414dec0a16c362b1f/collection"

Regenerated the IIIF to have the correct dat paths:

    npm run build

Then opened the dat link in beaker browser :-)