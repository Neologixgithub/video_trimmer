This is a cordova plugin to assist in several video editing tasks such as:

* Trimming


## Installation
```
cordova plugin add cordova-plugin-video-trimmer
```
`VideoTrimmer`  will be available in the window after deviceready.

## Usage

### Trim a Video
```javascript
VideoEditor.trim(
    trimSuccess,
    trimFail,
    {
        fileUri: 'file-uri-here', // path to input video
        trimStart: 5, // time to start trimming in seconds
        trimEnd: 15, // time to end trimming in seconds
        outputFileName: 'output-name', // output file name
        progress: function(info) {} // optional, see docs on progress
    }
);

function trimSuccess(result) {
    // result is the path to the trimmed video on the device
    console.log('trimSuccess, result: ' + result);
}

function trimFail(err) {
    console.log('trimFail, err: ' + err);
}