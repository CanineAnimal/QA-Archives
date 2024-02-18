This is a large repository. To upload without cloning its entire contents, clone in this manner:

```console
git clone --bare --single-branch --depth=1 --filter=blob:none <repo>
```

After cloning, set these environment variables when files are ready to be committed

```console
export GIT_DIR=$PWD/repo.git                  # bare repos don't have defaults for these
export GIT_WORK_TREE=$PWD                     # so supply some to suit our purpose
export GIT_INDEX_FILE=$GIT_DIR/scratch-index  # ...
```

Once PDFs are copied, add to repository in this manner:
```console
git read-tree --empty                       # make the index all pretty, and 
git add <Thread Folder Containing PDFs>/*  # everything's ordinary from here - add and 
git commit -m'Commit message'
```

Reference: https://stackoverflow.com/a/29396902         
