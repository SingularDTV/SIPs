---
SUP: 1
title: SUP Purpose and Guidelines
status: Implemented
author: Troy Murray (@dannydesert)
discussions-to: https://forum.snglsDAO.io/
created: 2020-07-23
updated: N/A
---

## What is an SUP?

SUP stands for SMDP Upgrade Proposal, it has been adapted from the EIP (Ethereum Improvement Proposal). The purpose of this process is to ensure changes to snglsDAO are transparent and well governed. An SUP is a design document providing information to the snglsDAO community about a proposed change to the system. The author is responsible for building consensus within the community and documenting dissenting opinions.

## What is an SCCP?

SCCP stands for SMDP Configuration Change Proposal. SCCP's are documents for making a case for modifying one of the system configuration variables. The intent is to provide a clear and detailed history behind each configuration change and the rationale behind it at the time it was implemented. The author of the document is responsible for building consensus within the community and documenting dissenting opinions.

## SUP & SCCP Rationale

We intend SUPs and SCCPs to be the primary mechanisms for proposing new features, collecting community input on an issue, and for documenting the design decisions for changes to to the SMDP. Because they are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

It is highly recommended that a single SUP contain a single key proposal or new idea. The more focused the SUP, the more successful it is likely to be.

An SUP or SCCP must meet certain minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement.

## SUP Work Flow

Parties involved in the process are the *author*, the [*SUP editors*](#SUP-editors), the [snglsDAO Core Contributors] and the snglsDAO community.

:warning: Before you begin, vet your idea, this will save you time. Ask the snglsDAO community first if an idea is original to avoid wasting time on something that will be rejected based on prior research (searching the Internet does not always do the trick). It also helps to make sure the idea is applicable to the entire community and not just the author. Just because an idea sounds good to the author does not mean it will have the intend effect. The appropriate public forum to gauge interest around your SUP or SCCP is [the SingularDTV Discord].

Your role as the champion is to write the SUP using the style and format described below, shepherd the discussions in the appropriate forums, and build community consensus around the idea. Following is the process that a successful SUP will move along:

```
[ WIP ] -> [ PROPOSED ] -> [ APPROVED ] -> [ IMPLEMENTED ] X [ REJECTED ] 
```

Each status change is requested by the SUP author and reviewed by the SUP editors. Use a pull request to update the status. Please include a link to where people should continue discussing your SUP. The SUP editors will process these requests as per the conditions below.

* **Work in progress (WIP)** -- Once the champion has asked the Synthetix community whether an idea has any chance of support, they will write a draft SUP as a [pull request]. Consider including an implementation if this will aid people in studying the SUP.
* **Proposed** If agreeable, SUP editor will assign the SUP a number (generally the issue or PR number related to the SUP) and merge your pull request. The SUP editor will not unreasonably deny an SUP. Proposed SUPs will be discussed on governance calls and in Discord. If there is a reasonable level of consensus around the change on the governance call the change will be moved to approved. If the change is contentious a vote of token holders may be held to resolve the issue or approval may be delayed until consensus is reached.
* **Approved** -- This SUP has passed community governance and is now being prioritised for development.
  
* **Implemented** -- This SUP has been implemented and deployed to mainnet.

* **Rejected** -- This SUP has failed to reach community consensus.

## What belongs in a successful SUP?

Each SUP or SCCP should have the following parts:

- Preamble - RFC 822 style headers containing metadata about the SUP, including the SUP number, a short descriptive title (limited to a maximum of 44 characters), and the author details.
- Simple Summary - “If you can’t explain it simply, you don’t understand it well enough.” Provide a simplified and layman-accessible explanation of the SUP.
- Abstract - a short (~200 word) description of the technical issue being addressed.
- Motivation (*optional) - The motivation is critical for SUPs that want to change Synthetix. It should clearly explain why the existing specification is inadequate to address the problem that the SUP solves. SUP submissions without sufficient motivation may be rejected outright.
- Specification - The technical specification should describe the syntax and semantics of any new feature.
- Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.
- Test Cases - Test cases may be added during the implementation phase but are required before implementation.
- Copyright Waiver - All SUPs must be in the public domain. See the bottom of this SUP for an example copyright waiver.

## SUP Formats and Templates

SUPs should be written in [markdown] format.
Image files should be included in a subdirectory of the `assets` folder for that SUP as follows: `assets/SUP-X` (for SUP **X**). When linking to an image in the SUP, use relative links such as `../assets/SUP-X/image.png`.

## SUP Header Preamble

Each SUP must begin with an [RFC 822](https://www.ietf.org/rfc/rfc822.txt) style header preamble, preceded and followed by three hyphens (`---`). This header is also termed ["front matter" by Jekyll](https://jekyllrb.com/docs/front-matter/). The headers must appear in the following order. Headers marked with "*" are optional and are described below. All other headers are required.

` SUP:` <SUP number> (this is determined by the SUP editor)

` title:` <SUP title>

` author:` <a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.>

` * discussions-to:` \<a url pointing to the official discussion thread at research.synthetix.io\>

` status:` < WIP | PROPOSED | APPROVED | IMPLEMENTED >

` created:` <date created on>

` * updated:` <comma separated list of dates>

` * requires:` <SUP number(s)>

` * resolution:` \<a url pointing to the resolution of this SUP\>

Headers that permit lists must separate elements with commas.

Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).

#### `author` header

The `author` header optionally lists the names, email addresses or usernames of the authors/owners of the SUP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the author header value must be:

> Random J. User &lt;address@dom.ain&gt;

or

> Random J. User (@username)

if the email address or GitHub username is included, and

> Random J. User

if the email address is not given.

#### `discussions-to` header

While an SUP is in WIP or Proposed status, a `discussions-to` header will indicate the URL at [forum.synthetix.io](https://forum.snglsDAO.io/) where the SUP is being discussed.

#### `created` header

The `created` header records the date that the SUP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

#### `updated` header

The `updated` header records the date(s) when the SUP was updated with "substantial" changes. This header is only valid for SUPs of Draft and Active status.

#### `requires` header

SUPs may have a `requires` header, indicating the SUP numbers that this SUP depends on.

## Auxiliary Files

SUPs may include auxiliary files such as diagrams. Such files must be named SUP-XXXX-Y.ext, where “XXXX” is the SUP number, “Y” is a serial number (starting at 1), and “ext” is replaced by the actual file extension (e.g. “png”).

## SUP Editors

The current SUP editors are

` * Troy Murray (@dannydesert)`

## SUP Editor Responsibilities

For each new SUP that comes in, an editor does the following:

- Read the SUP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the SUP for language (spelling, grammar, sentence structure, etc.), markup (Github flavored Markdown), code style

If the SUP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the SUP is ready for the repository, the SUP editor will:

- Assign an SUP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this SUP)

- Merge the corresponding pull request

- Send a message back to the SUP author with the next step.

Many SUPs are written and maintained by developers with write access to the Ethereum codebase. The SUP editors monitor SUP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on SUPs. We merely do the administrative & editorial part.

## History

The SUP document was derived heavily from the EIP Ethereum Improvement Proposal document in many places text was simply copied and modified. Any comments about the SUP document should be directed to the SUP editors. The history of the EIP is quoted below from the EIP document  for context:

* *"This document (EIP) was derived heavily from [Bitcoin's BIP-0001] written by Amir Taaki which in turn was derived from [Python's PEP-0001]. In many places text was simply copied and modified. Although the PEP-0001 text was written by Barry Warsaw, Jeremy Hylton, and David Goodger, they are not responsible for its use..."* *

June 10, 2019: SUP 1 has been drafted and submitted as a PR.


See [the revision history for further details](https://github.com/Synthetixio/), which is also available by clicking on the History button in the top right of the SUP.

### Bibliography

[the SingularDTV Discord]: https://discord.gg/a2E6uxk
[pull request]: https://github.comSingularDTV/SUPs/pulls
[markdown]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
[Bitcoin's BIP-0001]: https://github.com/bitcoin/bips
[Python's PEP-0001]: https://www.python.org/dev/peps/
[snglsDAO Engineering Team]: https://github.com/orgs/SingularDTV/people

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
