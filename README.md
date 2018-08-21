# QuickPreviewSample
This project attempts to implement the QuickLook Framework and its features.

Quick Look Framework provides previewing capabilities for documents that an app handles. Additionaly an activity controller (UIActivityViewController) can be presented for sending or sharing the previewed document.
The datasource for the document for preview is actually a list of NSURL objects specifying the path to each document. The Quick Look framework provides a view controller named QLPreviewController (Quick Look Preview Controller) for quick looking a document. Additionally, the framework requires the implementation of two datasource methods that belong to the QLPreviewControllerDataSource protocol in order for the preview to properly work. Besides that, there’s also the QLPreviewControllerDelegate protocol as well, which you can optionally implement and gain that way more control over the functionalities of the Quick Look framework.

In the project:

In the project you’ll find a collection of sample files that we’re going to preview in this demo app. Those files have been appended to the application’s bundle. We’ll create an array to provide the file names of the sample files existing to the bundle. Those file names will be used for two purposes:

1. In order to display the file name and description in our tableview properly.
2. Most importantly, to create the list of NSURL objects that the Quick Look framework needs as a datasource, so its capable of retrieving and previewing each file.

There are some supported methods of the QLPreviewItem protocol which could be useful to create a custom QLPreviewItem object.
One basic and simple rule is to make sure that the document you’re trying to preview can be actually opened by the Quick Look framework. by using the QLPreviewController class method named canPreviewItem(:).

Features Provided by the Quick Look Preview Controller: The Quick Look Preview Controller has a toolbar at the bottom with two bar button items. 
1. The first one on the left allows you to send and share the currently previewed document through an activity controller (UIActivityViewController).
2. The second bar button item in the right side presents a modal view controller with a list of all the available documents specified in the datasource.

The rest can be seen in the code.
