As of 6/12/20, the master branch of this repo fails on MacOS: it seems that [fsevents fails silently when watching 4097+ paths at once](https://github.com/fsnotify/fsevents/issues/48).

This branch confirms that the 4096-path limit is per-resource, not cumulative; here we have two resources with 4000 deps each, and Tilt has no problem watching files/detecting changes.
