# SpotMicroAI

This is the repository that contains the website.

The website can be found at https://spotmicroai.readthedocs.io/en/latest/

To build the website we use readthedocs.org.

This repository has 2 branches:
* master
* next

Master branch contains the current public website, is build at https://spotmicroai.readthedocs.io/en/latest/

Next branch contains the next public webstie, this is were the changes are made. Is build at https://spotmicroai.readthedocs.io/en/next/

Once next branch changes are made we just do the merge to the master branch.

```
git checkout master
git merge next
git push
```

If you are new to the community you can send merge request to the next branch, or if you are already a trusted developer in the community you can update the next branch yourself.