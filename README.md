# keystone-storage-namefunctions

Simple functions for generating filenames.

Bundled with [KeystoneJS](http://keystonejs.com)

## Included Methods

* `contentHashFilename` Calculate the filename from the sha1 hash of the file contents
* `originalFilename` Return the original filename provided in the file object
* `randomFilename` Generate a random filename

## `ensureCallback` utility

The `ensureCallback` method is also included, to standardise sync filename
method call signatures. Use it like this:

```js
var ensureCallback = require('keystone-storage-namefunctions/ensureCallback');
function originalFilename (file, index) {
	return file.originalname;
}
var asyncOriginalFilename = ensureCallback(originalFilename);
asyncOriginalFilename(file, index, function (err, result) {
	// result === file.originalname
});
```

## License

Licensed under The MIT License. Copyright (c) 2016 Jed Watson
