# Internal Documentation: Manually Testing the KnetMiner UI

## Overview
This page outlines the steps to use internally for manually testing the KnetMiner UI during development. It covers the various components of the UI and the different types of testing that can be performed.

### Table of Contents
#### Getting started
- [Prerequisites](#Prerequisites)

#### Various "Views" testing
- [Gene View](#gene-view)
- [Evidence View](#evidence-view)
- [Map View](#map-view)
- [Network View](#network-view)

#### Banner testing
- [Release notes](#release-notes)
- [Banner testing](#gene-view)

[Return to Table of Contents](#table-of-contents)

## Prerequisites
Before starting the testing process, ensure that the following pre-requisites are met:
- The latest version of the KnetMiner is cloned locally, and is running in your local browser (or on [Ci-Test](https://knetminer.com/ci-test/client/), if the test requires a larger dataset).
- You have cleared your browser cache. Here are some guides for doing it quickly, since during development you may find yourself clearing it often: [Chrome](https://chrome.google.com/webstore/detail/clear-cache/cppjkneekbjaeellbfkmgnhonkkjfpdn?hl=en), [Firefox](https://addons.mozilla.org/en-GB/firefox/addon/clearcache/) or [Safari](https://www.macrumors.com/how-to/clear-safari-cache/).

## Gene View
WIP

[Return to Table of Contents](#table-of-contents)

## Evidence View
WIP

[Return to Table of Contents](#table-of-contents)

## Map View
WIP

[Return to Table of Contents](#table-of-contents)

## Network View
WIP

[Return to Table of Contents](#table-of-contents)

## Release Notes
The KnetMiner release notes display a brief overview of the current KG supplying the instance a user is currently on.
1. Check that the icon is animating.
2. Ensure it is clickable and clicking on a grey area when it is open closes the release notes.
3. The release notes has a default format. From top to bottom:
* Title, description, what the KG contains, followed by a detailed breakdown.
Below is an example of what the release notes look like for the test instance as of 24/04/23. Remember that the KG version is based on the Ensembl version with which the KG was built.

<img src="https://user-images.githubusercontent.com/33641372/234048349-d4749676-425e-4052-bd6f-4da81aa3a9ba.png" width="400">

[Return to Table of Contents](#table-of-contents)

## Banner Testing
The app banner (from left to right):
1. KnetMiner Logo: hyperlinks to https://knetminer.com/products
2. Multispecies selector: opens as a dropdown with green on white text.
3. Release Notes button (see above).
4. Tutorial button: hyperlinks to https://knetminer.com/tutorial
5. Cite us button: hyperlinks to https://knetminer.com/knetminer-citation/how-to-cite.html
6. (Not Signed in shows a Sign In button) Login(Signed in)[Username] button, written with the user's username. Opens a popup with a menu leading to: "My Profile", "My Knetworks" And showing the user their email and organisation. Also allows the user to Sign out.
7. (Not Signed in shows a Sign up button: https://knetminer.com/beta/knetspace/sign-up/) (Signed in) My KnetSpace button: hyperlinks to https://knetminer.com/beta/knetspace/network/

The Beta instance has an additional grey banner on top of the normal KM banner, which prompts users for feedback. The button leads users here: https://knetminer.com/beta-feedback-form

![image](https://user-images.githubusercontent.com/33641372/234055284-93655ae0-48f0-4f0e-abec-e2bc7b31e29c.png)

[Return to Table of Contents](#table-of-contents)

## Conclusion
Testing the KnetMiner UI manually during development is an important step in ensuring its quality and functionality. By following these steps and performing the different types of testing, you can identify and fix issues before they affect end-users. Ideally, this should be combined with Selenium in later releases of KnetMiner (thinking 6.0+) 