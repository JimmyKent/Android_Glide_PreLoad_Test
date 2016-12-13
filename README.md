
参考网址：
http://stackoverflow.com/questions/38292729/glide-preload-only-works-if-size-is-specified
````
//图片预加载
  Glide.with(this)
  .load(mURL)
  .diskCacheStrategy(DiskCacheStrategy.SOURCE)
  .preload(1080, 1920);
````

````
//加载图片
  Glide.with(this).load(mURL)
  // Use the same dimensions used as when preloading.
  .override(1080, 1920)
  .dontTransform()
  .into(mImageView);
````
