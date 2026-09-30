# Reflink check

The GitHub Actions workflow runs on `ubuntu-latest` for pushes and manual dispatches. It creates a file, copies it with `cp --reflink=always`, and compares the contents. The job fails if the runner's filesystem does not support the reflink or the copy differs.
