Local AutoSave plugin for TinyMCE 4.x
=============

Save the TinyMCE (v4.x) content to LocalStorage* or SessionStorage* in your Browser to avoid losing your content in an page refresh, etc.

*Only if Browser supports webstorage. [See a list of Supported Browsers](http://www.html5rocks.com/features/storage#support).

*Cookie support has been disabled for now.

Demo
-----------

Do you want to see it in action? Visit [http://valtlfelipe.github.io/TinyMCE-LocalAutoSave/](http://valtlfelipe.github.io/TinyMCE-LocalAutoSave/).

Quick start
-----------

1. [Download a copy (.zip)](https://github.com/valtlfelipe/TinyMCE-LocalAutoSave/zipball/master).

2. Unzip the `localautosave` folder in your TinyMCE plugin folder `tinymce/plugins/`.

3. Initialize plugin and add it to the toolbar. Example:
```js
tinymce.init({
	plugins: "localautosave",
	toolbar1: "localautosave"
});
```

Translation
-----------

Currently available translations: `en`, `es`, `it`, `pt_BR`.

If you have translated this plugin, please create a pull request or send me a message so I can add your translation to this repository. Thanks!

Documentation
-------

You can configure this plugin using the methods listed here (those configurations are optional):

1. `las_seconds` => set the period to save the content in seconds (default 6).

2. `las_keyName` => set the key name for the LocalStorage, SessionStorage.

3. `las_callback` => fires an function with two variables in `this` object when content is saved successfully.

4. `las_nVersions` => number of versions of content you want to store (default 15, set 0 to disable) 

Example:
```js
tinymce.init({
	plugins: "localautosave",
	toolbar1: "localautosave",
	las_seconds: 15,
	las_nVersions: 15,
	las_keyName: "LocalAutoSave",
	las_callback: function() {
		var content = this.content; //content saved
		var time = this.time; //time on save action
	}
});
```

Thank you to [Valerio Gentile](https://github.com/dvcama) and [gastonsanguinetti](https://github.com/gastonsanguinetti) for contributing.

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/valtlfelipe/tinymce-localautosave/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

[![Analytics](https://ga-beacon.appspot.com/UA-10083241-13/TinyMCE-LocalAutoSave/readme?pixel)](https://github.com/igrigorik/ga-beacon)
