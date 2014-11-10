ios-asset-test
===

The purpose of this application is to determine which image assets are displayed by iOS when multiple resolutions (@1x, @2x, @3x) are present.

Three asset sets are used. The first only contains a @1x image. The second contains an @1x and @2x image. The third contains an @1x, @2x, and @3x image. Each of these three sets are pulled from the bundle, and from an asset catalog.

Known Issues
---

Currently, the only known issue is with the iPhone 6 Plus running iOS v8.1, built with Xcode v6.1:

 - If only the 1x image is available, it uses the 1x image, as expected.
 - If only 1x and 2x are available, it strangely uses the 1x instead of 2x. 
 - If 1x, 2x, and 3x are available, it uses the 3x, as expected.

This problem affects images used from the bundle, but doesn't seem to affect those in an asset catalog.