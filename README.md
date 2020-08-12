# LongAdjacency

A simple, all-client-side web app to transform Adjacency lists into Edge Lists.

## What is this?

Frequently, contact tracing data is recorded in a format like this:

| Individual | Contact1 | Contact2 | Contact 3 |
| ---------- | -------- | -------- | --------- |
| A          | B        | C        | D         |
| B          | A        | C        |           |

This is what we'll call an adjacency list. It's pretty readable, very understandable, and very easy to create in a tool like Microsoft Excel. If your individual recalls another contact, you can just add another column, easy-peasy. But then you need to do analysis with it and your analytic tools groan and complain and crash. These things HATE this format. It isn't [tidy](https://vita.had.co.nz/papers/tidy-data.pdf)!

There's another, better format out there. It's called an Edge list and it works like this:

| Individual | Contact |
| ---------- | ------- |
| A          | B       | 
| A          | C       |
| A          | D       |
| B          | A       |
| B          | C       |

Now, instead of having a row for each person, we have a row for each instance of contact between individuals. We've fundamentally altered the data's unit-of-analysis, translating the table into a [long](https://sejdemyr.github.io/r-tutorials/basics/wide-and-long/) format. It's still pretty readable, and your statistical algorithms will positively zip through it.

LongAdjacency is a tool designed to help you convert your data into Long format from Adjacency lists. Get it?

## How do I do it?

Just drag your adjacency list into the app and drop it. The app will parse the file and show you a preview of the table. Then you pick all your "ContactX" Columns (as in the example above) and the app will automatically wrangle the data into Edge list format. Once it looks alright, you can download the Edge list output.

## But this is PHI!

No worries! This application runs entirely on your computer--not on a server somewhere else. It's totally safe to load your PHI into it. If you're really paranoid, you can even load the web app and then *disconnect your computer from the internet* before loading your data in the app.

**General disclaimer** This repository was created for use by CDC programs to collaborate on public health related projects in support of the [CDC mission](https://www.cdc.gov/about/organization/mission.htm).  GitHub is not hosted by the CDC, but is a third party website used by CDC and its partners to share information and collaborate on software. CDC use of GitHub does not imply an endorsement of any one particular service, product, or enterprise. 
  
## Public Domain Standard Notice
This repository constitutes a work of the United States Government and is not
subject to domestic copyright protection under 17 USC § 105. This repository is in
the public domain within the United States, and copyright and related rights in
the work worldwide are waived through the [CC0 1.0 Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).
All contributions to this repository will be released under the CC0 dedication. By
submitting a pull request you are agreeing to comply with this waiver of
copyright interest.

## License Standard Notice
The repository utilizes code licensed under the terms of the Apache Software
License and therefore is licensed under ASL v2 or later.

This source code in this repository is free: you can redistribute it and/or modify it under
the terms of the Apache Software License version 2, or (at your option) any
later version.

This source code in this repository is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE. See the Apache Software License for more details.

You should have received a copy of the Apache Software License along with this
program. If not, see http://www.apache.org/licenses/LICENSE-2.0.html

The source code forked from other open source projects will inherit its license.

## Privacy Standard Notice
This repository contains only non-sensitive, publicly available data and
information. All material and community participation is covered by the
[Disclaimer](https://github.com/CDCgov/template/blob/master/DISCLAIMER.md)
and [Code of Conduct](https://github.com/CDCgov/template/blob/master/code-of-conduct.md).
For more information about CDC's privacy policy, please visit [http://www.cdc.gov/other/privacy.html](https://www.cdc.gov/other/privacy.html).

## Contributing Standard Notice
Anyone is encouraged to contribute to the repository by [forking](https://help.github.com/articles/fork-a-repo)
and submitting a pull request. (If you are new to GitHub, you might start with a
[basic tutorial](https://help.github.com/articles/set-up-git).) By contributing
to this project, you grant a world-wide, royalty-free, perpetual, irrevocable,
non-exclusive, transferable license to all users under the terms of the
[Apache Software License v2](http://www.apache.org/licenses/LICENSE-2.0.html) or
later.

All comments, messages, pull requests, and other submissions received through
CDC including this GitHub page may be subject to applicable federal law, including but not limited to the Federal Records Act, and may be archived. Learn more at [http://www.cdc.gov/other/privacy.html](http://www.cdc.gov/other/privacy.html).

## Records Management Standard Notice
This repository is not a source of government records, but is a copy to increase
collaboration and collaborative potential. All government records will be
published through the [CDC web site](http://www.cdc.gov).

## Additional Standard Notices
Please refer to [CDC's Template Repository](https://github.com/CDCgov/template)
for more information about [contributing to this repository](https://github.com/CDCgov/template/blob/master/CONTRIBUTING.md),
[public domain notices and disclaimers](https://github.com/CDCgov/template/blob/master/DISCLAIMER.md),
and [code of conduct](https://github.com/CDCgov/template/blob/master/code-of-conduct.md).
