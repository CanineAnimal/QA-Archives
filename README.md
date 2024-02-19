This is a large repository. If you want to use the console and upload without cloning its entire contents, clone in this manner (assuming Linux shell is used):

```console
git clone --no-checkout <repo>
git reset
```

Once PDFs are copied, add to repository in this manner:
```console
git add ThreadFolderName  					# everything's ordinary from here - add and 
git commit 									# make sure no archived threads are deleted!
```