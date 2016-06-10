## Simple example 


```html
<html>

<head>
  <title>QRCode.js</title>
  <script type="text/javascript" src="dist/qrcode.js"></script>
</head>
<body>
  <video width="320px" height="240px" id="video" autoplay></video>
</body>
<script>
function onSuccess(data) {
  document.getElementById('video').setAttribute("style", "border: 3px solid #52e250");
  console.log('Sucess:', data);
}

function onError(err) {
  console.error(err);
}
var qr = new QrReader({
  sucessCallback: onSuccess,
  errorCallback: onError,
  videoSelector: '#video',
  stopOnRead: true,
});
</script>

</html>
```