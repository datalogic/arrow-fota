# fota-agent

## Release version file

The `update-version` workflow creates `version.txt`, uploads it to the published
release, and commits a copy to `main`. The file does not need to exist beforehand.
Its contents are the release tag with a leading `v` removed (for example,
`v1.2.1` becomes `1.2.1`).

To update the latest release manually, run `update-version` from the Actions tab
using the `main` branch. Existing `version.txt` release assets are replaced.
After changing the workflow, use this manual trigger rather than rerunning an old
release job, which still uses the workflow from the original release tag.