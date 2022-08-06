# Fork of "PyXB Extended -- Python W3C XML Schema Bindings"

Upstream is https://github.com/renalreg/PyXB-X.

Branch `master` tracks upstream, while default branch `master-ga` tracks changes
made by Geoscience Australia. Make feature branches from `master-ga` and merge
them back to `master-ga`. Don't merge updates from upstream `master` into
`master-ga`, instead rebase `master-ga` on top of the latest `master` from
upstream, so that our changes always sit on top.

To rebase `master-ga`:

```
git clone git@github.com:GeoscienceAustralia/PyXB-X.git
cd PyXB-X
git remote add upstream https://github.com/renalreg/PyXB-X.git
git fetch upstream master
git switch master
git merge upstream/master --ff-only
git push origin master
git switch master-ga
git rebase master
git push master-ga -f
```

See upstream for original readme.
