# ckeditor-fileman-setting
for ckeditor fileman setting


# config.js

```
/**
 * @license Copyright (c) 2003-2017, CKSource - Frederico Knabben. All rights reserved.
 * For licensing, see LICENSE.md or http://ckeditor.com/license
 */

CKEDITOR.editorConfig = function( config ) {
	// Define changes to default configuration here. For example:
	// config.language = 'fr';
	// config.uiColor = '#AADC6E';
	config.toolbarGroups = [
		{ name: 'document', groups: [ 'mode', 'document', 'doctools' ] },
		{ name: 'clipboard', groups: [ 'clipboard', 'undo' ] },
		{ name: 'editing', groups: [ 'find', 'selection', 'spellchecker', 'editing' ] },
		'/',
		{ name: 'forms', groups: [ 'forms' ] },
		{ name: 'basicstyles', groups: [ 'basicstyles', 'cleanup' ] },
		{ name: 'paragraph', groups: [ 'list', 'indent', 'blocks', 'align', 'bidi', 'paragraph' ] },
		{ name: 'links', groups: [ 'links' ] },
		{ name: 'insert', groups: [ 'insert' ] },
		'/',
		{ name: 'styles', groups: [ 'styles' ] },
		{ name: 'colors', groups: [ 'colors' ] },
		{ name: 'tools', groups: [ 'tools' ] },
		{ name: 'others', groups: [ 'others' ] },
		{ name: 'about', groups: [ 'about' ] }
	];

	config.removeButtons = 'Form,Checkbox,Radio,TextField,Textarea,Button,Select,HiddenField,ImageButton,NewPage,Print,About,Language,SpecialChar,PageBreak,Smiley,Flash,Save';
	
	config.extraPlugins = 'autogrow,youtube,lightbox,bgimage';

	//config.extraPlugins = 'autogrow,youtube';
	config.autoGrow_onStartup = true;
	config.autoGrow_minHeight = 250;
	config.autoGrow_maxHeight = 600;
	config.autoGrow_bottomSpace = 10;

	//config.allowedContent = true;
	//config.htmlEncodeOutput = false;
	//config.entities = false;

	CKEDITOR.config.extraAllowedContent = 'a[data-lightbox,data-title,data-lightbox-saved]';
	
	var roxyFileman = '../plugins/fileman-1.4.5/index.html'; 

	config.filebrowserBrowseUrl = roxyFileman+'?integration=ckeditor';
	config.filebrowserImageBrowseUrl = roxyFileman+'?integration=ckeditor&type=image';
	config.removeDialogTabs = 'link:upload;image:upload';


	//config.extraPlugins = 'bgimage';
	//config.allowedContent = 'div{*}';
};
```
