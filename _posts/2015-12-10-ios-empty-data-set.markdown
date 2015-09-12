---
layout: post
title:  "iOS Empty DataSet"
date:   2015-12-10 17:46:33
categories: UITableView emptyset
---
Most applications use a special design for empty views (empty states of application)for having more impression on users and also better user experience . at this document you can find How to show a blank page in UITableview.


## Empty Data Set

Empty Views are helpful for Avoiding white-screens and communicating to your users why the screen is empty.

### How to use

*make an UIView nib file just like as “EmptyView.xib” in the project.
*insert an UIImageView and labels to design the empty data set. 
*to assign different values of image view and labels in various views , set a dictionary in “viewDidLoad” of each of your views

```objective-c
NSMutableDictionary *emptyViewInfo = [[NSMutableDictionary alloc] init];
[emptyViewInfo setValue:@"emptyView" forKey:@"image"];
[emptyViewInfo setValue:@"TableView is empty. Tap the rightBarButtonItem to insert row in the table view." forKey:@"text"];
```

* prepare a custom table with delegates:

```objective-c
-(void)showEmptyview;
-(void)hideEmptyview;
```
and override the “reloadData” of table with.

* use “EmptyTableViewController" classes if you want to show empty data set in “UITableViewController” ; and implement the delegates in it. you can also use the “EmptyViewController" classes if you choose the “UIViewController” to show your content.

* @interface FirstTableViewController : EmptyTableViewController

### Sample Code

A sample code of UITableView EmptyDataSet is available in [this repository](https://github.com/engmahsa/EmptyDataSet). 