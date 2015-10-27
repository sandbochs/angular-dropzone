# angular-dropzone
AngularJS directive for Dropzone.js

## Installation
```
bower install angular-dropzone4
```

You must add ngDropzone dependency to your app 

## Usage

### html

```
<form class="dropzone" method="post" enctype="multipart/form-data" ng-dropzone dropzone="dropzone" dropzone-config="dropzoneConfig">
  <input name="file" type="file" multiple />
</form>
```

### js
```
$scope.dropzoneConfig = {
  parallelUploads: 3,
  maxFileSize: 30,
  url: YOUR_UPLOAD_URL
};
```
