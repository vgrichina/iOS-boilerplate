What is IOS Boilerplate
-----------------------

Is a code base for iOS projects. Current version provides

  - BaseViewController with methods for secure handling of async http requests
  - ImageManager: a class for downloading images asynchronously
  - FastCell (inspired on [Atebits implementation](http://blog.atebits.com/2008/12/fast-scrolling-in-tweetie-with-uitableview/)) is a base class for implementing custom UITableViewCells with fast scrolling.
  - ListViewController: a base class for creating ViewControllers with one UITableView that can be refreshed with a pull-down component.
  - Place: a simple implementation of the MKAnnotation protocol
  - DictionaryHelper: an NSDictionary helper with methods for safe handling of collections
  - StringHelper: an NSString helper with methods for manipulating NSStrings. Including: trim, sha1 and urlEncode method.
  - DataHelper: an NSData helper with one method: hexString. It is used inside StringHelper to calculate the sha1 hash hexstring representation of a given string

The project contains some examples with the use of those utility classes:

  - Example that fetches a JSON object through an async HTTP request, and shows a progress HUD.
  - Example that fetches a single image with ImageManager
  - Example that combines FastCells with async image loading using ImageManager.
  - Example of variable height table cells using FastCell.
  - Example that shows how to extend ListViewController to create a tableview with a simple pull-down-to-refresh component.
  - Example that shows how to implement a swipeable cell
  - ViewController that uses MapOverlays and the Google Maps API to show the directions between two points.
  - Search bar that autocompletes locations.

Some screenshots:

![Demo menu](https://github.com/gimenete/iOS-boilerplate/raw/master/shots/demo-menu.png)

![Async cell images demo](https://github.com/gimenete/iOS-boilerplate/raw/master/shots/async-cells.png)

![Directions demo](https://github.com/gimenete/iOS-boilerplate/raw/master/shots/directions.png)


### Dependencies

IOS Boilerplate depends on the following third-party libraries:

  - [AFNetworking](https://github.com/AFNetworking/AFNetworking)
  - [SVProgressHUD](https://github.com/samvermette/SVProgressHUD)
  - [JSONKit](https://github.com/johnezang/JSONKit)
  - [EGOTableViewPullRefresh](https://github.com/enormego/EGOTableViewPullRefresh)

These are installed through the dependency manager [CocoaPods](https://github.com/CocoaPods/CocoaPods).

If you don’t use CocoaPods yet install it first as described in the CocoaPods [README](https://github.com/CocoaPods/CocoaPods/blob/master/README.md).

Now in the Terminal, from the root of the IOS Boilerplate clone, run the following commands to install the dependencies:

    $ pod install

After the installation has completed open up the Xcode workspace `IOSBoilerplate.xcworkspace` and you’re done.

It is simple to add or remove dependencies by updating the [Podfile](https://github.com/CocoaPods/iOS-boilerplate/blob/master/Podfile). A growing list of Pods are available from the [spec repo](https://github.com/CocoaPods/Specs).
