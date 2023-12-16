# Generate Release Notes
Generate release notes content for a release

## Inputs
* `tag`: The tag name for the release. This can be an existing tag or a new one.
  * Required: `true`
  * Default: `${{ github.ref_name }}`
  * Example: `v2`
* `base`: The name of the previous tag to use as the starting point for the release notes. Use to manually specify the range for the set of changes considered as part this release.
  * Required: `false`
  * Example: `v1`
* `token`: Github Token
  * Required: `true`
  * Default: `${{ github.token }}`
* `repository`: Repository to create the release for
  * Required: `true`
  * Default: `${{ github.repository }}`
  * Example: `swaglive/action-generate-release-notes`

## Outputs
* `name`: The generated name of the release
* `body`: The generated body describing the contents of the release supporting markdown formatting
