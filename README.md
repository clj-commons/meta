# clj-commons meta

This is a meta discussion repo for clj-commons issues. It's also the place to open an issue to suggest a project that clj-commons could adopt.

# community discussions:

## Slack:

You can join the channel #clj-commons on https://clojurians.slack.com

## Forum:

Clojureverse is a community forum for clojure, feel free also to write topic related to clj-commons if you like this kind of communication


# What to do

If you use a project that's in need of tlc, please file an issue about it, so we can start working on transferring it to clj-commons.

If you'd like to help out maintaining any of the projects maintained by clj-commons, you can file an issue about that too.

If there's stuff you think clj-commons should be doing, but is not, guess what, you may very well file an issue for that.

# General principles

* Respect the wishes of maintainers - If clj-commons goes around forking lots of projects, that is bound to create ill-will in the community. The goal of this is not empire building, it’s helping keep the Clojure ecosystem healthy.
* Provide value to the community - There are lots of unmaintained Clojure projects that are not that important. There are also lots of old libraries which are just stable and run fine. We only have a limited amount of time and attention, we should focus it on places where we can provide the biggest improvements.

# Entry Criteria

Before adopting a project into clj-commons, there are some entry criteria that need to be satisfied:

* The project is 'unmaintained'. This is subjective, and there are many libraries which are just 'done'. Indications that a project is unmaintained could be: the library breaking with new Java or Clojure versions, issues and PRs not being addressed for years, no recent releases, no commits for years, or the maintainer is no longer involved with Clojure.
* The project is notable, useful, and currently being used by people. This is inherently subjective, but some evidence for this could be number of stars on GitHub, recent issues/PRs, number of downloads on Clojars, how much work went into creating it, or if any notable projects depend on it. An example of a project that wouldn't be accepted is a small library created by one person that only they use.
* There is at least one person who wants to be a maintainer of the project. These maintainers will be listed in a `CODEOWNERS` file. We don’t want the new home of the project to become unmaintained as well.
* We have attempted to talk to the original owner of the project and they are happy to transfer the project. The goal is not to be forking projects away from people who want to manage the project themselves.

# Maintenance Criteria

Minimum requirements for projects in clj-commons:

* Passing continuous integration
* Responsive to issues and pull requests
* Documentation ([cljdoc.org](https://cljdoc.org) makes this very easy)
* Regularly creating releases
* Staying up to date with new Clojure and JVM releases
* Use preferably [Circleci](https://circleci.com/) instead of Travis for the ci of the repository. (this will more coherent along all the projects maintained)

# When to use the `clj-commons` Maven group ID vs. the original group ID

If an existing project is being transferred to clj-commons, then we should try and use the original Maven group ID if possible. This requires the original maintainer add a clj-commons team member as a Clojars collaborator.

This is because there is currently no good way to communicate to dependency tooling like lein-ancient that the artifact which was once maintained under `group-x/project-y` is now maintained under `clj-commons/project-y`.

If the original maintainer can't be contacted to transfer Clojars admin rights, then it will be necessary to switch the group ID to `clj-commons`. In this case, it is a good idea to add a note to the README explaining the change, and the original lineage of the project.

# Sponsorship

clj-commons is a loosely formed organization which does not accept sponsorships on behalf of its maintainers. This does not mean that you cannot sponsor the maintainers directly if they accept sponsorship. Anotherway of contributing back to the community would be to sponsor [Clojurists Together](https://www.clojuriststogether.org), allthough there is no guarantee that such a sponsorship would directly benefit clj-commons.
