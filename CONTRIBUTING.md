---
layout: default
title: Join us
image: /images/about.jpg
---

# Contributing


[![NordicESMhub chat](https://img.shields.io/badge/zulip-join_chat-brightgreen.svg)](https://nordicesmhub.zulip.org)



[Nordic Earth System Modeling hub][nordicesmhub-site] is an open source project,
and we welcome contributions of all kinds:

- new tools/workflows/jupyter notebooks to analyze/visualize Earth System Models (NorESM, CESM, Oslo-CTM3, FLEXPART, etc.) over the Nordic countries 
- new training materials,
- fixes to existing material,
- bug reports,
- reviews of proposed changes are all welcome.

## Contributor Agreement

By contributing, you agree that we may redistribute your work under [our license](LICENSE.md).
In exchange, we will address your issues and/or assess your change proposal as promptly as we can, acknowledge
your contributions and help you become a member of our community.
Everyone involved in [Nordic Earth System Modeling hub][nordicesmhub-site]
agrees to abide by our [code of conduct](CODE_OF_CONDUCT.md).

## How to Contribute

The easiest way to get started is to file an issue
to tell us about a spelling mistake,
some awkward wording,
or a factual error.
This is a good way to introduce yourself
and to meet some of our community members.


1.  If you have a [GitHub][github] account,
    or are willing to [create one][github-join],
    but do not know how to use Git,
    you can report problems or suggest improvements by [creating an issue][issues].
    This allows us to assign the item to someone
    and to respond to it in a threaded discussion.

2.  If you are comfortable with Git,
    and would like to add or change material,
    you can browse the list of existing issues (see [below](#where-to-contribute))
	and submit a pull request (PR).
    Instructions for doing this are [included below](#using-github).

## Where to Contribute

[NordicESMhub repositories](https://github.com/NordicESMhub) have many open issues where you are welcome to contribute.

1.  If you wish to change this repository,
    please work in <https://github.com/NordicESMhub/nordicesmhub.github.io>,
    which can be viewed at <https://nordicesmhub.github.io/>.

2.  If you wish to change another repository in the NordicESMhub organization,
    please review CONTRIBUTING.md guideline of the corresponding repository. In the 
	[section below](#what-to-contribute), we list priority areas but these are mostly
	to help you to find where to contribute.

3.  If you wish to add a new repository in the NordicESMhub organization, 
    create a [new issue](https://github.com/NordicESMhub/nordicesmhub.github.io/issues/new)
	in this repository. Do not forget to mention the purpose of your issue.

## What to Contribute

There are many ways to contribute,
from writing new tools and improving existing ones
to updating or filling in the documentation
and submitting [bug reports][issues]
about things that don't work, aren't clear, or are missing.
If you are looking for ideas, please see the 'Issues' tab for
a list of issues associated with each repository.

Comments on issues and reviews of pull requests are just as welcome:
we are smarter together than we are on our own.
Reviews from novices and newcomers are particularly valuable:
it's easy for people who have been using these lessons for a while
to forget how impenetrable some of this material can be,
so fresh eyes are always welcome.

### Priorities

Here is a non-exhaustive list of repositories for which we need your help:

- [NordicESMHub website](https://github.com/NordicESMhub/nordicesmhub.github.io): the overall structure of the website has been defined
  but many sections are still empty. See [issues](https://github.com/NordicESMhub/nordicesmhub.github.io/issues) to know more on where to contribute.
- [Geofag-docs](https://github.com/NordicESMhub/geofag-docs): if you are working in Norway at the University of Oslo, you may be interested in contributing to the Geofag documentation.
  The objective is to migrate the current [Geosciences Modeling Wiki](https://wiki.uio.no/mn/geo/geoit/index.php/Welcome_to_Geosciences_Modeling_Wiki) to [Geofag-docs](https://uio-geofag-docs.readthedocs.io/en/latest/).
  However, we would like to mostly enumerate what is UiO specific and have the more general documentation in [NordicESMhub website](https://nordicesmhub.github.io/).
- [ESM conda tools](https://github.com/NordicESMhub/esmconda-recipes)
- [Galaxy Climate tools](https://github.com/NordicESMhub/galaxy-tools). See [issues](https://github.com/NordicESMhub/galaxy-tools/issues) to know what we need in priority. Have a look to the list of [projects](https://github.com/NordicESMhub/galaxy-tools/projects) that are aiming to demonstrate the use of climate data for multidisciplinary studies.
- [Oslo-CTM3 documentation](https://github.com/NordicESMhub/OsloCTM3-docs) which you can view [here](https://osloctm3-docs.readthedocs.io/en/latest/).
- [NorESM documentation](https://github.com/NorESMhub/NorESM-docs) which you can view [here](https://noresm-docs.readthedocs.io/en/latest/).

## Using GitHub

If you choose to contribute via GitHub, you may want to look at
[How to Contribute to an Open Source Project on GitHub][how-contribute].
To manage changes, we follow [GitHub flow][github-flow].

Each issues and pull requests are reviewed by volunteers and we also encourage you to do so.
The repository owners have final say over what gets merged into the lesson so it is often good practice to discuss your plans in an issue
before you implement anything.

To use the web interface for contributing to a lesson:

1.  Fork the originating repository to your GitHub profile.
2.  Within your version of the forked repository, move to the `master` branch and
create a new branch for each significant change being made.
3.  Navigate to the file(s) you wish to change within the new branches and make revisions as required.
4.  Commit all changed files within the appropriate branches.
5.  Create individual pull requests from each of your changed branches
to the `master` branch within the originating repository.
6.  If you receive feedback, make changes using your issue-specific branches of the forked
repository and the pull requests will update automatically.
7.  Repeat as needed until all feedback has been addressed.

When starting work, please make sure your clone of the originating `master` branch is up-to-date
before creating your own revision-specific branch(es) from there.
Additionally, please only work from your newly-created branch(es) and *not*
your clone of the originating `master` branch.


## Other Resources

General discussion of [Nordic Earth System Modeling hub][nordicesmhub-site]
happens on the [Nordic ESM hub zulip][nordicesmhub-zulip],
which everyone is welcome to join.

[nordicesmhub-zulip]: https://nordicesmhub.zulipchat.com/
[nordicesmhub-site]: https://nordicesmhub.github.io/
[github]: https://github.com
[github-flow]: https://guides.github.com/introduction/flow/
[github-join]: https://github.com/join
[how-contribute]: https://egghead.io/series/how-to-contribute-to-an-open-source-project-on-github
[issues]: https://guides.github.com/features/issues/
