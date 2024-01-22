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

**Pull requests that are submitted without going through this process may be closed without review.**

The **sole exception** to this process is if you're submitting a pull request making a very low-impact modification, such as a cosmetic improvement or fixing a link in documentation.
For those, you can go ahead and just submit a pull request.
If you're not sure if your change would be considered a low-impact modification, follow the steps above.
Anything that changes code would not be considered a low-impact modification and should go through the above process.

Again, this process is designed primarily to avoid wasted time on your part - for example, to prevent you from doing work that would sit without review for an unacceptable amount of time, or just wouldn't end up being merged because it adds functionality that is not aligned with planned directions for the repository.

If you're looking to develop new analytic functionality, we *strongly* encourage you to consider building and distributing your own QIIME 2 plugin(s) as opposed to starting with contributions to the plugins in this organization.
That allows you to move quickly and doesn't require any feedback or review from the QIIME 2 team (but we're of course happy to provide support and feedback on the QIIME 2 Forum).
You can even use the QIIME 2 Forum to advertise and provide support for your plugin.
We cover that briefly in the next section, and in more detail in [Developing with QIIME 2](https://cap-lab.bio/developing-with-qiime2/).

## Building your own plugins and interfaces

You don't need approval from existing QIIME 2 developers or maintainers to create and distrubute your own tools, such as plugins, that build on QIIME 2.
We encourage you to build your own.
[Developing with QIIME 2](https://cap-lab.bio/developing-with-qiime2/) is the primary resource for learning how to build and share your QIIME 2-based tools, and we are happy to support developers in the [Developer Discussion on the QIIME 2 Forum](https://forum.qiime2.org/c/dev-discussion).

You can build your QIIME 2 tools in your own way - your new tool doesn't need to live in our GitHub organization, or be part of one of the existing QIIME 2 distributions, and in fact it's probably better for it to start independently.
The *tiny* and *amplicon* distributions, in particular, are focused on providing a stable and reliable experience to their many users all over the world, and as a result change fairly slowly.
If you're working on cutting edge tools that are evolving rapidly, you should build those on your own and can share them with the community as [Community Contributions on the QIIME 2 Forum](https://forum.qiime2.org/c/community-contributions/15).
You can also have your users request help on the QIIME 2 Forum, but be aware that the forum moderators will almost certainly reach out to you to reply to help requests since they won't necessarily be experts in your tools (and are already tied up providing tech support to the community).
