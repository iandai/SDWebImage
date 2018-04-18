<p align="center" >
  <img src="SDWebImage_logo.png" title="SDWebImage logo" float=left>
</p>


## Features

- [x] Fetch security image URL. In order to protect image resources, instead of using a pernement image url, using a temporary security url only valid for short seconds. imageManager:fetchSecurityURL: is used to handle this situation.


## How To Use

```objective-c
#import <SDWebImage/UIImageView+WebCache.h>
...

SDWebImageManager.sharedManager.delegate = self;

- (nullable NSURL *)imageManager:(nonnull SDWebImageManager *)imageManager fetchSecurityURL:(nullable NSURL *)imageURL {
    NSURL *tempURL = [self fetchSecurityURLMethod];
    return tempURL;
}

[imageView sd_setImageWithURL:[NSURL URLWithString:@"http://www.domain.com/path/to/image.jpg"]
             placeholderImage:[UIImage imageNamed:@"placeholder.png"]];
```


