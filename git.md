# Show me what changed
# -C = detect renames, -M40 = consider a delete/add pair to be a rename if no more than 40% of file changed
`git diff -C -M40 <commit-hash>`

# Create git tag with a message
`git tag -a 1.1 -m "Release version 1.1 with changes to UI"`


# List all tags, with at most x lines of output (if annotated tag).
`git tag -nx`

# Eg, show all tags with at most 2 lines from tag message:
`git tag -n2`


# Git diff output linewrap
If using less as pager (the default?) type -S while viewing the diff to reenable line wrapping

# Show tracked files on whatever HEAD is pointing at
`git ls-tree -r HEAD --name-only`
