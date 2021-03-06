# Redactor plugin for Craft

This plugin adds a “Redactor” field type to Craft CMS, which provides a rich text editor powered by [Redactor] by Imperavi.

## Requirements

This plugin requires Craft CMS 3.0.0-RC11 or later.

## Installation

To install the plugin, follow these instructions.

1. Open your terminal and go to your Craft project:

        cd /path/to/project

2. Then tell Composer to load the plugin:

        composer require craftcms/redactor

3. In the Control Panel, go to Settings → Plugins and click the “Install” button for Redactor.

## Configuration

### Redactor Configs

You can create custom Redactor configs that will be available to your Redactor fields. They should be created as JSON files in your `config/redactor/` folder.

For example, if you created a `config/redactor/Standard.json` file with the following content: 

```json
{
    "buttons": ["format", "bold", "italic", "lists", "link", "file", "horizontalrule"],
    "plugins": ["source", "fullscreen"]
}
```

…then a “Standard” option would become available within the “Redactor Config” setting on your Redactor field’s settings.

See the [Redactor documentation] for a list of available config options.

### HTML Purifier Configs

You can create custom HTML Purifier configs that will be available to your Redactor fields. They should be created as JSON files in your `config/htmlpurifier/` folder.

See the [HTML Purifier documentation] for a list of available config options. 

### Redactor JS Plugins

The [Fullscreen], [Source Code], [Table], and [Video] Redactor JS plugins are bundled by default. If you wish to install any additional Redactor JS [plugins], just place their JS file (and CSS file if there is one) in `craft/config/redactor/plugins/`. Both files should have the exact same name as the plugin ID that you will be typing into the `plugins` array in your Redactor config JSON.  

[Redactor]: https://imperavi.com/redactor/
[Redactor documentation]: https://imperavi.com/redactor/docs/settings/
[HTML Purifier documentation]: http://htmlpurifier.org/live/configdoc/plain.html
[Fullscreen]: https://imperavi.com/redactor/plugins/fullscreen/
[Source Code]: https://imperavi.com/redactor/plugins/source/
[Table]: https://imperavi.com/redactor/plugins/table/
[Video]: https://imperavi.com/redactor/plugins/video/
[plugins]: https://imperavi.com/redactor/plugins/
