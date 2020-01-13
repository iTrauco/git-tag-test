testing git push v2.2

ref
https://itrau.co/git-tags

'error: src refspec v2.2 does not match any
error: failed to push some refs to 'https://github.com/iTrauco/git-tag-test.git'

solved by 

https://itrau.co/3845uB4

3877

Maybe you just need to commit. I ran into this when I did:

mkdir repo && cd repo
git remote add origin /path/to/origin.git
git add .
Oops! Never committed!

git push -u origin master
error: src refspec master does not match any.
All I had to do was:

git commit -m "initial commit"
git push origin master
Success!
