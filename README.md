<div align="center">

# VRC Packaging Action

[![Generic badge](https://img.shields.io/github/release/VRLabs/VRCTools-Packaging-Action?display_name=tag&label=Release)](https://github.com/VRLabs/VRCTools-Packaging-Action/releases/latest)
[![Generic badge](https://img.shields.io/badge/License-MIT-informational.svg)](https://github.com/VRLabs/VRCTools-Packaging-Action/blob/main/LICENSE)

[![Generic badge](https://img.shields.io/discord/706913824607043605?color=%237289da&label=DISCORD&logo=Discord&style=for-the-badge)](https://discord.vrlabs.dev/)
[![Generic badge](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Fshieldsio-patreon.vercel.app%2Fapi%3Fusername%3Dvrlabs%26type%3Dpatrons&style=for-the-badge)](https://patreon.vrlabs.dev/)

GitHub Action to package Unity assets in both `unitypackage` and `vcc` package formats. It is based on the VRLabs [`VRC Packaging Tool`](https://github.com/VRLabs/VRCTools-Packaging).

### ⬇️ [Check out on the Github Action Marketplace](https://github.com/marketplace/actions/vrc-packaging-action)

</div>

---

## Inputs

### `path`

**Required** The path to the package folder.

### `outputPath`

**Required** The output directory path.

### `releaseUrl`

The release URL to set in the `package.json`.

### `unityReleaseUrl`

The release URL to set in the `package.json` for the unitypackage version.

### `releaseVersion`

The version to set in the `package.json`. If not specified it will be taken from the `package.json`.

### `noVcc`

Skips the build of the `vcc` package, the `package.json` will not contain an url for the unitypackage version.

### `noUnityPackage`

Skips the build of the `unitypackage`.

### `customJsonFields`

Customized fields to add to the `package.json`, in the form of a list of `key=value`

## Outputs

### `vccPackagePath`

The path of the exported `vcc` package.

### `unityPackagePath`

The path of the exported `unitypackage`.

### `serverPackageJsonPath`

The path of the exported `server-package.json`. contains some more informations compared to the one included in the packages, useful for repository listings

## Example usage

```yaml
uses: VRLabs/VRCTools-Packaging-Action@v1
with:
  path: 'Path/To/Asset'
  outputPath: 'Packages'
  releaseUrl: 'https://url/to/package.id-x.x.x.zip'
```

## VCC only example


```yaml
uses: VRLabs/VRCTools-Packaging-Action@v1
with:
  path: 'Path/To/Asset'
  outputPath: 'Packages'
  releaseUrl: 'https://url/to/package.id-x.x.x.zip'
  noUnityPackage: 'true'
```

## Example that includes extra fields to `package.json`

```yaml
uses: VRLabs/VRCTools-Packaging-Action@v1
with:
  path: 'Path/To/Asset'
  outputPath: 'Packages'
  releaseUrl: 'https://url/to/package.id-x.x.x.zip'
  customJsonFields: |
    "changelogUrl=https://link.to.changelog"
    "category=essentials"
```

## Contributors

* [Cibbi](https://github.com/Cibbi)
* [JelleJurre](https://github.com/jellejurre)

## License

VRLabs VRC Packaging Action is available as-is under MIT. For more information see [LICENSE](https://github.com/VRLabs/VRC-Packaging-Action/blob/main/LICENSE).

## Contact us

If you need help, our support channel is on [Discord](https://discord.vrlabs.dev). 

<div align="center">

[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/VRLabs.png" width="50" height="50">](https://vrlabs.dev "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Discord.png" width="50" height="50">](https://discord.vrlabs.dev/ "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Patreon.png" width="50" height="50">](https://patreon.vrlabs.dev/ "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Twitter.png" width="50" height="50">](https://twitter.com/vrlabsdev "VRLabs")

</div>


