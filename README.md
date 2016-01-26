# angular-dropzone
AngularJS directive for Dropzone.js

## Installation
```
bower install angular-dropzone
```

## Usage

### html

Include `bower_components/dropzone/downloads/dropzone.min.js` and `bower_components/angular-dropzone/lib/angular-dropzone.js` in your html file. Also include `bower_components/dropzone/downloads/css/dropzone.css` for basic styling.

Add `ngDropzone` as a dependency to your module and initialize the Dropzone directive by including it in your template.

```
<form class="dropzone"
      method="post"
      enctype="multipart/form-data"
      ng-dropzone
      dropzone="ctrl.dropzone"
      dropzone-config="ctrl.dropzoneConfig"
      event-handlers="{ 'addedfile': self.dzAddedFile, 'error': self.dzError }">
</form>
```

### js

```
myModule.controller('DemoController', [function() {
  var self = this;

  self.dzAddedFile = function( file ) {
    console.log( file );
  };
  
  self.dzError = function( file, errorMessage ) {
    console.log(errorMessage);
  };
  
  self.dropzoneConfig = {
    parallelUploads: 3,
    maxFileSize: 30
  };
}]);
```

To get a list of all the events, go to http://www.dropzonejs.com/#events and read through the events list.
