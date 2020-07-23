# SUPs [![Discord](https://img.shields.io/discord/413890591840272394.svg?color=768AD4&label=discord&logo=https%3A%2F%2Fdiscordapp.com%2Fassets%2F8c9701b98ad4372b58f13fd9f65f966e.svg)](https://discordapp.com/channels/413890591840272394/) [![Twitter Follow](https://img.shields.io/twitter/follow/snglsDAO.svg?label=snglsDAO&style=social)](https://twitter.com/snglsDAO)
Synthetix Improvement Proposals (SUPs) describe standards for the Synthetix platform, including core protocol specifications, client APIs, and contract standards.

WIP: A browsable version of all current and draft SUPs can be found on [the official SUP site](https://SUPs.synthetix.io/).

# Contributing

 1. Review [SUP-1](SUPS/SUP-1.md).
 2. Fork the repository by clicking "Fork" in the top right.
 3. Add your SUP to your fork of the repository. There is a [template SUP here](SIP-X.md).
 4. Submit a Pull Request to snglsDAO's [SUPs repository](https://github.com/snglsDAO/SUPs).

Your first PR should be a first draft of the final SUP. It must meet the formatting criteria enforced by the build (largely, correct metadata in the header). An editor will manually review the first PR for a new SUP and assign it a number before merging it. Make sure you include a `discussions-to` header with the URL to a new thread on [research.synthetix.io](https://research.synthetix.io) where people can discuss the SUP as a whole.

If your SUP requires images, the image files should be included in a subdirectory of the `assets` folder for that SUP as follow: `assets/SUP-X` (for SUP **X**). When linking to an image in the SUP, use relative links such as `../assets/SUP-X/image.png`.

When you believe your SUP is mature and ready to progress past the WIP phase, you should ask to have your issue added to the next governance call where it can be discussed for inclusion in a future platform upgrade. If the community agrees to include it, the SUP editors will update the state of your SUP to 'Approved'. 

# SUP Statuses

* **WIP** - a SUP that is still being developed.
* **Proposed** - a SUP that is ready to be reviewed in a governance call.
* **Approved** - a SUP that has been accepted for implementation by the Synthetix community.
* **Implemented** - a SUP that has been released to mainnet.
* **Rejected** - a SUP that has been rejected.


# Validation

SUPs must pass some validation tests.  The SUP repository ensures this by running tests using [html-proofer](https://rubygems.org/gems/html-proofer) and [SUP_validator](https://rubygems.org/gems/SIP_validator).

It is possible to run the SUP validator locally:
```
gem install SUP_validator
SUP_validator <INPUT_FILES>
```


# Automerger

The SUP repository contains an "auto merge" feature to ease the workload for SUP editors.  If a change is made via a PR to a draft SUP, then the authors of the SUP can Github approve the change to have it auto-merged by the [SUP-automerger](https://github.com/bakaoh/SIP_automerger) bot.
