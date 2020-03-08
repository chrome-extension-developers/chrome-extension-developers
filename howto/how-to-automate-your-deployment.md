# How to automate your extension deployment

If you have develop a chrome extension, you may want to apply the concepts of Continuous Integration (CI) and Continuous Deployment (CD) to it.

One option is using [Travis CI][travis-ci] and [chrome-webstore-upload-cli][cwu-cli].

Here are some references:
- [chrome-webstore-upload-cli][cwu-cli] (GitHub repo)
  - `README.md` - Initial, setup adn usage instructions for this command line tool
  - `Travis autoupload guide.md` - a short guide on how to setup _Travis CI_ for publishing the extension
- [podStation][podStation] - (GitHub repo) - a extension that is published with `chrome-webstore-upload-cli` - it automatically decides whether to publish the extension by comparing the version from `manifest.json` to the last _tag_ used on the git repository
  - `.travis.yml` - _Travis CI_ configuration
  - `check_should_deploy_and_create_new_tag.sh` - Script that checks if it is a new version and show be published (also creates a zip file for upload)

[travis-ci]: https://travis-ci.com/
[cwu-cli]: https://github.com/DrewML/chrome-webstore-upload-cli
[podStation]: https://github.com/podStation/podStation
