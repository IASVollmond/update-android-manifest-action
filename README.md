# Update Android Manifest Action

This action update the `versionCode` and `versionName` properties of the AndroidManifest.xml file for your Android projects.

## Inputs

### `package-name`

**Required** The value of the package name

### `android-manifest-path`

**Required** The relative path for the AndroidManifest.xml file.

### `version-code` 
  
**Required** The value of the version code, this must be between 0 and 2100000000.

###  `version-name`
    
**Required** The value of the version name

###  `print-file`

Output the AndroidManifest.xml file in console before and after update.

## Usage

```yaml
- name: Update AndroidManifest.xml
  uses: damienaicheh/update-android-version-manifest-action@v1.1.0
  with:
    android-manifest-path: './path_to_your/AndroidManifest.xml'
    package-name: 'com.example.name'
    version-code: 2
    version-name: '2.0'
    print-file: true
```
