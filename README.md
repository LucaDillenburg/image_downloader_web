# Image downloader for web

Download images from URL on Flutter Web

## Download image on webb

```dart

final WebImageDownloader _webImageDownloader = WebImageDownloader();
const _url = "https://picsum.photos/200";

Future<void> _downloadImage() async {
  await _webImageDownloader.downloadImageFromWeb(_url);
}

```

&nbsp;

### Download image with reduced quality

```dart

final WebImageDownloader _webImageDownloader = WebImageDownloader();
const _url = "https://picsum.photos/200";

Future<void> _downloadImage() async {
  await _webImageDownloader.downloadImageFromWeb(_url, imageQuality: 0.5);
}
```

&nbsp;

### Download image with custom headers

```dart

final WebImageDownloader _webImageDownloader = WebImageDownloader();
const _url = "https://picsum.photos/200";

Future<void> _downloadImage() async {
  final Map<String, String> headers = {
    'authorization': token,
  };
  await _webImageDownloader.downloadImageFromWeb(_url, headers: headers);
}
```
