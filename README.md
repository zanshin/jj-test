# jj-test
Experiments with using Jujutsu (jj) and Git side-by-side

# Simulate adding Jujutsu to an existing Git repository
## Create some commits using Git

    nvim test-a.md
    nvim test-b.md
    nvim test-c.md

# Add Jujutsu
## Setup colocated jj repository

    jj init git --colocate

## Associate remote bookmarks (branches) with local repository

    jj bookmark track main@origin

## Create bookmark (branch) and then pull request

    jj edit <change id>
    jj bookmark create doc/readme
    jj git push -b doc/readme --allow-new --remote origin
