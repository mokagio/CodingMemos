iOS Memos
=========

####Simulator Location

`~/Library/Application Support/iPhone Simulator/`, _I've forgotten this like 1000 times!_

####Dismiss the keyboard

```objc
[viewThatLoadedTheKeyboard resignFirstResponder]
```

In a simple configuration with a `UIViewController` which has some `UITextField`s a way to dismiss the keyboard is to make the controller the `delegate` of the inputs and then implement:

```objc
-(BOOL)textFieldShouldReturn:(UITextField *)textField
{
    if (textField == self.textFieldThatShouldDismissTheKeyboard) {
        [textField resignFirstResponder];
        return NO;
    } 
    return YES;
}
```

####Focus on view that loads a user input
For example a UITextField, which loads the keyboard

```objc
[inputView becomeFirstResponder];
```
	
####Hide the navigation bar

```objc
aUINavigationControllerInstance.navigationBarHidden = YES;
```
	
####Hide the status bar

In the `Info.plist`, add the entry: **UIStatusBarHidden, YES** or **Status bar is initally hidden, YES**.	

#### Open link in Safari

```
NSURL *url = [NSURL URLWithString:@"http://www.stackoverflow.com"];
if (![[UIApplication sharedApplication] openURL:url]) {
    NSLog(@"%@%@",@"Failed to open url:",[url description]);
}
```
	
####UITableViewCell height

The height of the UITableViewCells in a table view is actually controlled by the table view itself. Do:

```objc
CGFloat newHeight = 80;
tableView.rowHeight = newHeight;
```
	
iOS Tips
========

####Subview superview's center evaluation
When evaluating the center of the superview, use width / 2, or height / 2, rather than the center property. _Explain why, even if it obvious_

iOS Libraries
=============

##AFNetworking

####Reading the response headers

```objc
AFHTTPRequestOperationManager *manager = [AFHTTPRequestOperationManager manager];
[manager POST:urlString
       parameters:paramsDictionary
          success:^(AFHTTPRequestOperation *operation, id responseObject) {
              // Log the headers
              NSLog(@"%@", operation.response.allHeaderFields);
              
              //...
          } failure:^(AFHTTPRequestOperation *operation, NSError *error) {
              //...
          }];
```
