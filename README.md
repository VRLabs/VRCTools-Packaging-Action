# VRLabs VRC Packaging Action
[![Generic badge](https://img.shields.io/github/release/VRLabs/VRC-Packaging-Action?display_name=tag&label=Release)](https://github.com/VRLabs/VRC-Packaging-Action/releases/latest)
[![Generic badge](https://img.shields.io/badge/License-MIT-informational.svg)](https://github.com/VRLabs/VRC-Packaging-Action/blob/main/LICENSE) 

This GitHub Action packages Unity assets in both `unitypackage` and `vcc` package formats. It is based on the `vrctools-packaging` Docker image.

## Inputs

### `path`

**Required** The path to the folder to package

### `outputPath`

**Required** The output directory path for the packages.

### `releaseUrl`

The release URL to set in the `package.json`.

### `noVcc`

Skips the build of the `vcc` package, the `package.json` will not contain an url for the unitypackage version.

### `noUnityPackage`

Skips the build of the `unitypackage`.

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
  releaseUrl: 'https://github.com/User/Asset/releases/download/master/package.id-x.x.x.zip'
```

## VCC only example


```yaml
uses: VRLabs/VRCTools-Packaging-Action@v1
with:
  path: 'Path/To/Asset'
  outputPath: 'Packages'
  releaseUrl: 'https://github.com/User/Asset/releases/download/master/package.id-x.x.x.zip'
  noUnityPackage: 'true'
```

## License

VRLabs VRC Packaging Action is available as-is under MIT. For more information see [LICENSE](https://github.com/VRLabs/VRC-Packaging-Action/blob/main/LICENSE).

## Contact us

If you need help, our support channel is on [Discord](https://discord.vrlabs.dev). 

