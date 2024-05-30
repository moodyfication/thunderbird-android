# ItemTouchHelper

This is a copy of the `ItemTouchHelper` class and its helpers from [AndroidX RecyclerView](https://developer.android.com/jetpack/androidx/releases/recyclerview) 1.2.1.

It was modified to support swipe actions that don't remove the item from the list, i.e. our swipe actions "toggle selection", "mark as read/unread", "add/remove star". For those actions the view is animated back into its original position instead of off the screen.

Changes to this class should be limited to the functional changes we need. The aim is to make it easier to rebase on AndroidX's version of `ItemTouchHelper`.
This means…

- we're not converting this class to Kotlin unless AndroidX changes their version,
- we're ignoring warnings generated by unmodified code,
- and we're leaving API checks that could be removed because our minSdkVersion is higher than that of the AndroidX library.