# Quadra Creek manifest

Manifests for Quadra Creek releases and development

`default.xml` - manifest for Quadra Creek development

```
repo init -u https://github.intel.com/quadra-creek/manifest.git
```

`v<X>.<Y>.xml` - manifest for Quadra Creek releases

As example, checking out v0.1 release:

```
repo init -u https://github.intel.com/quadra-creek/manifest.git -m v0.1.xml -b refs/tags/v0.1
```

The versioned manifests are kept on master branch but they are only valid when there's a tag for that version already, so it's advised to pass the -b option to make sure you are building a valid version.
