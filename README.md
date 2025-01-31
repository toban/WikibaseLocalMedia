# Wikibase Local Media

[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/ProfessionalWiki/WikibaseLocalMedia/CI/master)](https://github.com/ProfessionalWiki/WikibaseLocalMedia/actions?query=workflow%3ACI)
[![Latest Stable Version](https://poser.pugx.org/professional-wiki/wikibase-local-media/version.png)](https://packagist.org/packages/professional-wiki/wikibase-local-media)
[![Download count](https://poser.pugx.org/professional-wiki/wikibase-local-media/d/total.png)](https://packagist.org/packages/professional-wiki/wikibase-local-media)
![GitHub](https://img.shields.io/github/license/ProfessionalWiki/WikibaseLocalMedia)

MediaWiki extension that adds support for local media files to [Wikibase] via a new data type.

Wikibase Local Media was created by [Professional.Wiki] with Funding from [Rhizome]. It is an open source project and contributions are welcome!

[Professional.Wiki] provides commercial [Wikibase hosting], [MediaWiki development] and support.

## Demo and screenshot

<a href="https://www.youtube.com/watch?v=mK-zdazdH78"><img src=".github/youtube.png" width="430px" title="Play video" /></a>
<a href="https://user-images.githubusercontent.com/146040/94343935-0e10d300-001c-11eb-8ec2-6f86ccf20e2f.png">
<img src="https://user-images.githubusercontent.com/146040/94343935-0e10d300-001c-11eb-8ec2-6f86ccf20e2f.png" width="400px" title="View image" />
</a>

Also see [this animated gif](https://twitter.com/i/status/1286293710112731137).

## Platform requirements

* [PHP] 7.2 or later, including PHP 8.0
* [MediaWiki] 1.34, 1.35 or 1.36
* [Wikibase Repository] REL1_34 or REL1_35 (probably also REL1_36)

See the [release notes](#release-notes) for more information on the different versions of this extension.

## Installation

First install MediaWiki and Wikibase Repository.

**Using Composer (option 1/2)**

The recommended way to install Wikibase Local Media is using [Composer](https://getcomposer.org) with
[MediaWiki's built-in support for Composer](https://professional.wiki/en/articles/installing-mediawiki-extensions-with-composer).

On the commandline, go to your wikis root directory. Then run these two commands:

```shell script
COMPOSER=composer.local.json composer require --no-update professional-wiki/wikibase-local-media:*
composer update professional-wiki/wikibase-local-media --no-dev -o
```

**Manual download (option 2/2)**

You can also install the extension via git clone or download. Place the `WikibaseLocalMedia` directory into `extensions`.

**Enabling the extension**

Then enable the extension by adding the following to the bottom of your wikis `LocalSettings.php` file:

```php
wfLoadExtension( 'WikibaseLocalMedia' );
```

You can verify the extension was enabled successfully by opening your wikis Special:Version page in your browser.

Finally, please consider [sponsoring the project].

## Running the tests

* PHP tests: `php tests/phpunit/phpunit.php extensions/WikibaseLocalMedia/tests/`
* JS tests: `index.php?title=Special%3AJavaScriptTest&filter=jquery.ui.mediasuggester`

## Release notes

### Version 1.0.1

Released on March 17th 2021

* Allowed installation with PHP 7.2.x

### Version 1.0.0

Released on October 5th 2020

* Added optional integration with Wikibase Client

### Version 0.2.1

Released on September 28th 2020

* Fixed support for PHP 7.3.x

### Version 0.2

Released on September 26th 2020

* Added support for MediaWiki/Wikibase 1.35
* The extension is now listed in the Wikibase group on Special:Version

### Version 0.1

Released on September 26th 2020

* [Initial release] for MediaWiki/Wikibase 1.34

[Professional.Wiki]: https://professional.wiki
[Wikibase]: https://wikibase.consulting/what-is-wikibase/
[Rhizome]: https://rhizome.org/
[MediaWiki]: https://www.mediawiki.org
[PHP]: https://www.php.net
[Wikibase Repository]: https://www.mediawiki.org/wiki/Extension:Wikibase_Repository
[LocalSettings.php]: https://www.mediawiki.org/wiki/Manual:LocalSettings.php
[MediaWiki development]: https://professional.wiki/en/mediawiki-development
[Wikibase hosting]: https://professional.wiki/en/hosting/wikibase
[sponsoring the project]: https://github.com/sponsors/JeroenDeDauw
[Initial release]: https://professional.wiki/en/news/wikibase-local-media
