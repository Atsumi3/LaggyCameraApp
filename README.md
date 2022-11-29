# LaggyCameraApp

Android12 で WebView上のカメラ映像表示がおかしくなる問題があったので、その検証アプリ

アプリサイズを小さくするためにJavaで最小構成で設定

検証用サイト
https://practice-75a12.web.app/

```html
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Welcome to Firebase Hosting</title>
</head>

<body>
  <video id="video" playsinline></video>
  <script type="text/javascript">
    var constraints = { video: { width: 200, height: 200, facingMode: "user" } };
    navigator.mediaDevices.getUserMedia(constraints)
      .then(function (mediaStream) {
        var video = document.querySelector('video');
        video.srcObject = mediaStream;
        video.onloadedmetadata = function (e) {
          video.play();
        };
      })
      .catch(function (err) { alert(err.name + ": " + err.message); });
  </script>
</body>

</html>
```
