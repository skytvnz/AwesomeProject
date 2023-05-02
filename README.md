**com.google.android.webview** update restarts **RN Android app** when **fetch()** is used

This is standard AwesomeProject with an additional fetch call in `App.tsx.` Check line **66** in `App.tsx`
``` 
    fetch("http://example.com/movies.json").then(response => {
      return response.json();
    }).then(res => {
      console.log('res', res)
    }).catch(err => console.error(err));
```

# Steps to reproduce

1. yarn install
2. yarn release
3. Connect your Android device via adb
4. yarn install-release-apk
5. Launch AwesomeProject app from Android phone
5. Go to Android settings, find the WebView app, uninstall updates
6. Observe that AwesomeProject app restarted

The same can be seen when updating to the latest **com.google.android.webview** or by manually installing different versions of Webview using the link below


# Web view versions
https://android-system-webview.en.uptodown.com/android/versions



