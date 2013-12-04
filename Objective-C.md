Objective-C Memos
=================

####Static arrays
Just use the C style.

```objective-c
static CGFloat arrayOfFloats[] = { 1.1, 2.2, 3.3 };
```

####Typedef a block

```objective-c
typedef void (^Callback)();
typedef void (^CallbackWithParameter)(NSObject *aParameter);
```

###Using a block as a method argument

```obj-c
- (void)methodWithBlockAsParameter:(void(^)())block;
```
