# Update Android Manifest Action

Custom-GitHub-Action, um während eines Workflows die Werte 'package', 'version-Code' und 'versionName' der AndroidManifest.xml zu manipulieren.

Die Action manipuliert die XML nur bei Laufzeit des Workflows. Das heißt die .apk-Datei, die über den Workflow gebaut wird, beinhaltet diese, aber es findet keine Veränderung des Quellcodes statt.

Repository ist ein Detached Fork von https://github.com/damienaicheh/update-android-version-manifest-action.

## Parameter

### `package-name`

**Required** Wert, der für 'package' im Android-Manifest eingesetzt wird. Als String-Wert mitgeben.

### `android-manifest-path`

**Required** Der Pfad, der zu "AndroidManifest.xml" zeigt. Als String-Wert mitgeben.

### `version-code` 
  
**Required** Der Wert des Versioncodes. Dieser muss zwischen 0 und 2100000000 liegen. Als Integer-Wert mitgeben.

###  `version-name`
    
**Required** Der Wert des Versionsnamen. Als String-Wert mitgeben.

###  `print-file`

Vor und nach dem Update wird das AndroidManifest in den Output geschrieben. Als Boolean-Wert mitgeben.

## Nutzung

```yaml
- name: Update AndroidManifest.xml
  uses: IASVollmond/update-android-version-manifest-action@main
  with:
    android-manifest-path: './Iaswebde.MDE.Android/Properties/AndroidManifest.xml'
    package-name: 'com.Iaswebde.Mde'
    version-code: 122525000
    version-name: '1.2.2525.00'
    print-file: true
```
