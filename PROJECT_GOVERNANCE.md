Each project under clj-commons needs to have at least a maintainer, and the names of the maintainers should be listed
 in the `.github/CODEOWNERS` file. The organization as such does not pose any
 restrictions on how the individual projects are run, other than what is stated in the
 [meta/README](https://github.com/clj-commons/meta/README.md).

  This means that PR review protocol, release cycles, and post-release announcements are up to the
 maintainer of the project, even though we encourage announcing new releases to the [official Clojure Google Group](https://groups.google.com/group/clojure)
 and the `#announcements` channel in the [Clojurians slack](https://clojurians.slack.com). Also, coding style is up to the maintainers of
 the project, but clj-commons recommends following [The Clojure Style Guide](https://github.com/bbatsov/clojure-style-guide).

# Continuous Integration

Because clj-commons as an organization is most familiar with [CircleCI](https://circleci.com), we recommend using CircleCI
 as a project's CI tool. Note that CircleCI Github application is already configured at the organization level. Simply dropping a valid configuration ([check the official documentation](https://circleci.com/docs/2.0/language-clojure/)) is enough to enable Continuous Integration (of branches and pull requests).

# Transfer vs Forking

When a project is adopted into clj-commons, a transfer of ownership should be preferred over forking.
 There are several reasons for this:

1. The adoption is somewhat formalized and friendly, the original authors need to give their blessing for
 this to happen,
1. All GitHub metainfo, stars, issues, PRs, etc are transferred in a transfer, but lost in a fork.

We should resort to forking only if the original maintainers remain unresponsive to our inquiries.
 Currently, unresponsive means not having replied to our request within two months of repeated outreach.

# Artefact Coordinates

As with transfer vs forking, artefact coordinates also need consideration. There are limitations to
 how Clojars work, which makes it hard for a Clojars group to change ownership of a single artefact
 within a group. This means that for certain organizations/authors, it is impossible to let clj-commons
 continue artefact publication under their group. Even so, we prefer to keep the artefact coordinates
 because this will let tools like [lein-ancient](https://github.com/xsc/lein-ancient) continue to work
 also with projects that are moved to clj-commons.
