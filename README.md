WearHttp
======
This library provides an http contents getter.

## Example
### Code in AndroidWear app
```java
new WearGetText(MainActivity.this).get("http://example.com/text.txt", 
  new WearGetText.WearGetCallBack() {
    @Override
    public void onGet(String contents) {
        mTextView.setText(contents);
    }

    @Override
    public void onFail(final Exception e) {
        mTextView.setText(e.getMessage());
    }
});
new WearGetImage(MainActivity.this).get("https://example.com/image.png", 
  new WearGetImage.WearGetCallBack() {
    @Override
    public void onGet(Bitmap image) {
        mImageView.setImageBitmap(image);
    }

    @Override
    public void onFail(final Exception e) {
        mTextView.setText(e.getMessage());
    }
});
```
### AndroidWear screen shot  
![image](https://cloud.githubusercontent.com/assets/1386930/4348768/7b2bb5f0-419a-11e4-946b-1587e970b6e9.png)  


## Usage  
In mobile project and wear module build.gradle.
```groovy
repositories {
    maven { url 'http://raw.github.com/takahirom/WearHttp/master/repository/' }
}
dependencies {
    ...
    compile 'com.kogitune:wear-http:0.0.2'
}
```

In wear module. You implement it as in the [Example](#example)


## License

This project is released under the Apache License, Version 2.0.

* [The Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)
