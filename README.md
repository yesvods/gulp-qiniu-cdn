![qiniu](http://assets.qiniu.com/qiniu-409x220.png)
# gulp-qiniu-cdn

> Gulp plugin for qiniu to upload file stream.

# Install

Install with [npm](https://npmjs.org/)

```
npm install --save-dev gulp-qiniucdn
```

# Usage

The following example will show the minimal usage with gulp-qiniu-cdn

```
var gulp = require('gulp'),
    qiniuCDN = require('gulp-qiniu-cdn');

gulp.task('qiniu', function () {
    return gulp.src(['app/**/*.css','app/**/*.js'])
        .pipe(qiniuCDN({
          AK: Your ACCESS_KEY,
            SK: Your SECRET_KEY,
            scope: bucketname
        }))
});
```

Optional configurations are available.For more detail about configuation ,see [offical document](http://developer.qiniu.com/docs/v6/sdk/nodejs-sdk.html).

```
{
  scope,
  callbackUrl,
    callbackBody,
    returnUrl,
    returnBody,
    asyncOps,
    endUser,
    expires,
    params,
    mimeType,
    crc32,
    checkCrc
}
```

# License
Copyright (c) 2015, Jogis. (MIT License)
