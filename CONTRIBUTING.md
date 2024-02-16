# Contributing to the QIIME 2 Ecosystem

There are many ways to contribute to the QIIME 2 ecosystem, and you don't have to be a software developer to help out!
Contributions can come in the form of: new documentation; improvements to existing documentation; assistance with technical support on the [QIIME 2 Forum](https://forum.qiime2.org); code providing new features, bug fixes, or usabililty improvements to existing functionality; reporting of bugs or feature requests on the project's GitHub issue trackers; development of new plugins or interfaces; providing constructive feedback on how we can improve QIIME 2; and other ways.
Regardless of your background, we'd love to help you figure out how to contribute.

## I just have a question

If you have a question or need help with QIIME 2, refer instead to our [Support Guidelines](https://github.com/qiime2/.github/blob/main/SUPPORT.md).

## Contributing to repositories in the `qiime2` GitHub organization

If you'd like to contribute to one of the repositories in the `qiime2` GitHub organization there are a few steps to follow.
These are in place to respect everyone's time: yours as the contributor, and ours as the reviewers.

1. First, **before doing other work related to the contribution that you'd like to make**, create an issue on the repository that you would be contributing to stating what you'd like to contribute and why you think this would be a useful contribution.
   If you don't know what repository to create an issue on, start with a post on the [QIIME 2 Forum](https://forum.qiime2.org) and we can help you figure that out.
2. Next, keep an eye on that issue (e.g., by monitoring GitHub notifications). The repository maintainer(s) may have questions or feedback, and this will ultimately lead to an approval of the issue or closing of the issue.
   You may have to be patient - as of this writing, we can't commit to a specific timeline to reply to new issues.
3. If approved, you can begin working on your contribution.
   **Maintainer approval of your issue is a commitment to a timely review of your contribution**, so this should move forward at an acceptable pace from this point.
   You can find documentation on setting up your QIIME 2 development environment in [Developing with QIIME 2](https://cap-lab.bio/developing-with-qiime2/).
4. When you have a final draft of your code that you think is ready for review, you can [submit a pull request](https://docs.github.com/en/pull-requests).
   Just as we commit to a timely review of your code when we approve your issue, **our expectation is that if you submit a pull request you'll be responsive to feedback that we give in a timely manner**.

**Pull requests that are submitted without going through this process may be closed without review.**

The **sole exception** to this process is if you're submitting a pull request making a very low-impact modification, such as a cosmetic improvement or fixing a link in documentation.
For those, you can go ahead and just submit a pull request.
If you're not sure if your change would be considered a low-impact modification, follow the steps above.
Anything that changes code would not be considered a low-impact modification and should go through the above process.

Again, this process is designed primarily to avoid wasted time, on your end and on our end. For example, this process will prevent you from doing work that would sit without review for an unacceptable amount of time, or just wouldn't end up being merged because it adds functionality that is not aligned with planned directions for the repository.

If you're looking to develop new analytic functionality, we *strongly* encourage you to consider building and distributing your own QIIME 2 plugin(s) as opposed to starting with contributions to the plugins in this organization.
That allows you to move quickly and doesn't require any feedback or review from the QIIME 2 team (but we're of course happy to provide support and feedback on the QIIME 2 Forum).
You can even use the QIIME 2 Forum to advertise and provide support for your plugin.
We cover that briefly in the next section, and in more detail in [Developing with QIIME 2](https://cap-lab.bio/developing-with-qiime2/).

## Building your own plugins and interfaces

You don't need approval from existing QIIME 2 developers or maintainers to create and distribute your own tools, such as plugins, that build on QIIME 2.
This is the beauty of the plugin-based architecture of QIIME 2: development of tools for introducing novel functionality can be distributed by anyone, removing the lead development team as a bottleneck or gatekeeper between developers of new functionality and users interested in that functionality, and customized QIIME 2 distributions can be created and shared by users.
We encourage you to build your own tools if you would like to introduce new functionality into the QIIME 2 ecosystem, or alter the functionality of existing plugins or interfaces.
[Developing with QIIME 2](https://cap-lab.bio/developing-with-qiime2/) is the primary resource for learning how to build and share your QIIME 2-based tools, and we are happy to support developers in the [Developer Discussion on the QIIME 2 Forum](https://forum.qiime2.org/c/dev-discussion).

You can build your QIIME 2 tools in your own way - your new tool doesn't need to live in our GitHub organization or be part of one of the QIIME 2 distributions developed and maintained in the [Caporaso Lab](https://cap-lab.bio).
You can use the [Community Contributions topic on the QIIME 2 Forum](https://forum.qiime2.org/c/community-contributions/15) to share your plugins with QIIME 2 users.
You can also have your users request help on the QIIME 2 Forum, but if you go this route (as opposed to, for example, directing users to your email, GitHub issue tracker, or another forum for technical support) you should monitor the forum (e.g., via forum notifications) to answer user questions about your plugin. 
Please be aware that the forum moderators will not be able to provide support for your plugins and may reach out to you to reply to help requests since they won't necessarily be experts in your tools (and are already tied up providing tech support to the community).

### Guidance on maximizing compatibility between your plugin(s) and existing QIIME 2 distribution(s)

If you want your QIIME 2 plugin(s) to work with existing QIIME 2 distribution(s), your focus should be on maximizing compatibility between your plugin(s) and the relevant QIIME 2 distribution(s).
To do this, you should observe the types and formats that are used in the target distribution(s), and make your functionality compatible with those.
Avoid defining new types and formats when you can reuse existing ones, to maximize compatibility and interoperability (as well as reducing your own time cost!). A partial list of common semantic types can be found in the [QIIME 2 documentation](https://docs.qiime2.org/), and a complete list of types and formats available in a local installation of QIIME 2 can be accessed with the `qiime tools list-types` and `qiime tools list-formats` commands.
If you do need to create new types and formats, you can add these directly in your own plugin(s).

The Caporaso Lab is not taking on new responsibility for distributing plugins right now (i.e., integrating them in the conda metapackages they develop and maintain; note that "conda metapackage" and "distribution" are essentially synonymous in this context).
You should consider those existing distributions to be foundations that you can build on with your plugin(s), or you can create and distribute your own conda metapackages. Guidance on each of these approaches:
   - Your install instructions can indicate that a user should install whichever distribution you depend on (tiny, amplicon, shotgun, ...) and then illustrate how to install your plugin(s) in that environment however it makes sense (conda, pip, ...).
   - Alternatively, you can compose and share your own distribution of plugins (e.g., building from the tiny distribution) that captures the set of functionality you’d like to share.
   - Either of these approaches is totally fine. The former is an easier starting point.

The weekly dev builds of the QIIME 2 distributions can help you make sure your code stays current with the distribution(s) you are targeting as you can automate your testing against them.
See [here](https://cap-lab.bio/developing-with-qiime2/plugins/how-to-guides/set-up-development-environment.html) for instructions on setting up a development environment (that documentation URL is subject to change while *[Developing with QIIME 2](https://cap-lab.bio/developing-with-qiime2/)* is being written).
Following those instructions will install the most recent successful development metapackage build (again, usually weekly, but sometimes they fail).

You can request feedback on your plugin as a whole from more experienced QIIME 2 developers by reaching out on the [Developer Discussion on the QIIME 2 Forum](https://forum.qiime2.org/c/dev-discussion).
However, be cognizant of the fact that doing code review takes a long time to do well: you should request this when you feel like you have a final draft of the plugin that you'd like to release.
Please have others who you work closely with -- ideally experienced software developers, and even more ideally experienced QIIME 2 plugin developers -- review it first.
If you have questions along the way, you can ask those whenever - just be sure to review *[Developing with QIIME 2](https://cap-lab.bio/developing-with-qiime2/)* and search the forum in case your question has already been answered previously.

Thanks for your interest in building with QIIME 2 -- see you on the QIIME 2 Forum! 🚀
