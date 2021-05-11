⚠️ Relocation warning
=====================

This repository has been relocated to [the new organization Kaleidos Ventures](https://github.com/kaleidos-ventures/taiga-contrib-protected/) where the team will continue developing Taiga. Please, follow us and contribute on the new location. New issues should be placed as well under the new Github organization.

We haven't archived this repository yet because we want to keep the issues currently open, but it'll become inactive eventually and so it will be archived.

## Taiga Contrib Protected

Taiga-contrib-protected is a plugin (installed in taiga-back) that offers an alternative storage system for Taiga. 
It works in conjunction with taiga-protected service and requires a specific Nginx configuration.
- Refer to the official [documentation](https://taigaio.github.io/taiga-doc/dist/setup-production.html#taiga-back) to 
  install it.
- Refer to the official [documentation](https://taigaio.github.io/taiga-doc/dist/setup-production.html#install-protected)
  to install the service
- Refer to the official [documentation](https://taigaio.github.io/taiga-doc/dist/setup-production.html#nginx) 
  to configure Nginx

### Configuration
The configuration variables for this plugin are:

```python
#########################################
## Media Static settings
#########################################

MEDIA_URL = "https://media-domain.example.com/"
MEDIA_ROOT = "/path/to/media"
DEFAULT_FILE_STORAGE = "taiga_contrib_protected.storage.ProtectedFileSystemStorage"
THUMBNAIL_DEFAULT_STORAGE = DEFAULT_FILE_STORAGE
```

They are located in `settings/config.py.prod.example`

## Vendoring

How to update vendored libraries.

```
pip install -t taiga_contrib_protected/_vendor -r taiga_contrib_protected/_vendor/vendor.txt --no-compile --no-deps
rm -rf taiga_contrib_protected/_vendor/*.dist-info
```

## Documentation

Currently, we have authored three main documentation hubs:

- **[API](https://taigaio.github.io/taiga-doc/dist/api.html)**: Our API documentation and reference for developing from 
  Taiga API.
- **[Documentation](https://taigaio.github.io/taiga-doc/dist/)**: If you need to install Taiga on your own server, 
  this is the place to find some guides.
- **[Taiga Resources](https://resources.taiga.io)**: This page is intended to be the support reference page for the 
  users.

## Bug reports

If you **find a bug** in Taiga you can always report it:

- in [Taiga issues](https://tree.taiga.io/project/taiga/issues). **This is the preferred way**
- in [Github issues](https://github.com/taigaio/taiga-contrib-protected/issues)
- send us a mail to support@taiga.io if is a bug related to [tree.taiga.io](https://tree.taiga.io)
- send us a mail to security@taiga.io if is a **security bug**.

One of our fellow Taiga developers will search, find and hunt it as soon as possible.

Please, before reporting a bug, write down how can we reproduce it, your operating system, your browser and version, and if it's possible, a screenshot. Sometimes it takes less time to fix a bug if the developer knows how to find it.

## Community

If you **need help to setup Taiga**, want to **talk about some cool enhancemnt** or you have **some questions**, please write us to our [mailing list](https://groups.google.com/d/forum/taigaio).

If you want to be up to date about announcements of releases, important changes and so on, you can subscribe to our newsletter (you will find it by scrolling down at [https://taiga.io](https://www.taiga.io/)) and follow [@taigaio](https://twitter.com/taigaio) on Twitter.

## Contribute to Taiga

There are many different ways to contribute to Taiga's platform, from patches, to documentation and UI enhancements, just find the one that best fits with your skills. Check out our detailed [contribution guide](https://resources.taiga.io/extend/how-can-i-contribute/)

## Code of Conduct

Help us keep the Taiga Community open and inclusive. Please read and follow our [Code of Conduct](https://github.com/taigaio/code-of-conduct/blob/master/CODE_OF_CONDUCT.md).

## License

Every code patch accepted in Taiga codebase is licensed under [AGPL v3.0](http://www.gnu.org/licenses/agpl-3.0.html). You must be careful to not include any code that can not be licensed under this license.

Please read carefully [our license](https://github.com/taigaio/taiga-contrib-protected/blob/master/LICENSE) and ask us if you have any questions as well as the [Contribution policy](https://github.com/taigaio/taiga-contrib-protected/blob/master/CONTRIBUTING.md).
