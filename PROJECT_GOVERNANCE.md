Each project under clj-commons need to have at least a maintainer, and the names of the maintainers should be listed
 in the `.github/CODEOWNERS` file. The organization as such do not pose any 
 restrictions on how the individual projects are run, other than what is stated in the 
 [meta/README](https://github.com/clj-commons/meta/README.md).

  This means that PR review protocol, release cycles, and post-release annoncements are up to the 
 maintainer of the project, even though we encourage announcing new releases to the main Google Group
 and the #announcement channel in the Clojurians slack. Also, coding style is up to the maintainers of
 the project, but clj-commons recommend following [The Clojure Style Guide](https://github.com/bbatsov/clojure-style-guide)

  #Continious Integration
 As clj-commons as an org is most familiar with [CircleCI](https://circleci.com), we recommend using CircleCI
 as a projects CI tool.

  # Transfer vs forking
 When a project is adopted to clj-commons, a transfer of ownership should be preferred over forking.
 There are several reasons for this:

  1) The adoption is somewhat formalized and friendly, the original authors need to give their blessing for
 this to happen.

  2) All github metainfo, stars, issues, PRs, etc are transferred in a transfer, but lost in a fork

  We should resort to forking only if the original maintainers remain unresponsive to our inquiries. 
 Currently, unresponsive means not having replied to our request within two months of repeated outreach.

  # Artefact coordinates
 As with transfer vs forking, artefact coordinates also need consideration. There are limitations to 
 how Clojars work, which makes it hard for a Clojars group to change ownership of a single artefact 
 within a group. This means that for certain organizations/authors, it is impossible to let clj-commons
 continue artefact publication under their group. Even so, we prefer to keep the artefact coordinates 
 because this will let tools like [lein-ancient](https://github.com/xsc/lein-ancient) continue to work
 also with projects that are moved to clj-commons.
