# Assignment-1
.................ASSIGNMENT-1.....................

1(a)

(i)
E:\>cd ps

E:\ps>mkdir Assignment-1

E:\ps>cd Assignment-1

E:\ps\Assignment-1>git init
Initialized empty Git repository in E:/ps/Assignment-1/.git/

E:\ps\Assignment-1>echo "one two three" >> file1.txt

E:\ps\Assignment-1>git add.
git: 'add.' is not a git command. See 'git --help'.

The most similar command is
        add

E:\ps\Assignment-1>git add .

E:\ps\Assignment-1>git commit -m "1st commit"
[master (root-commit) 4d41724] 1st commit
 1 file changed, 1 insertion(+)
 create mode 100644 file1.txt
----------------------------------------------------------------------------
(ii)
E:\ps\Assignment-1>git remote add origin https://github.com/damusey/Assignment-1.git

E:\ps\Assignment-1>git push origin master
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 227 bytes | 227.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/damusey/Assignment-1.git
 * [new branch]      master -> master
------------------------------------------------------------------------------
(iii)
E:\ps\Assignment-1>git branch Delivery

E:\ps\Assignment-1>git branch QA

E:\ps\Assignment-1>git branch Feature

E:\ps\Assignment-1>git branch Dev

E:\ps\Assignment-1>git branch Prod
-------------------------------------------------------------------------------
(iv)
E:\ps\Assignment-1>git push origin QA
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'QA' on GitHub by visiting:
remote:      https://github.com/damusey/Assignment-1/pull/new/QA
remote:
To https://github.com/damusey/Assignment-1.git
 * [new branch]      QA -> QA

E:\ps\Assignment-1>git push origin Feature
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'Feature' on GitHub by visiting:
remote:      https://github.com/damusey/Assignment-1/pull/new/Feature
remote:
To https://github.com/damusey/Assignment-1.git
 * [new branch]      Feature -> Feature

E:\ps\Assignment-1>git push origin Prod
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'Prod' on GitHub by visiting:
remote:      https://github.com/damusey/Assignment-1/pull/new/Prod
remote:
To https://github.com/damusey/Assignment-1.git
 * [new branch]      Prod -> Prod

E:\ps\Assignment-1>git push origin Dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'Dev' on GitHub by visiting:
remote:      https://github.com/damusey/Assignment-1/pull/new/Dev
remote:
To https://github.com/damusey/Assignment-1.git
 * [new branch]      Dev -> Dev

E:\ps\Assignment-1>git push origin Delivery
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'Delivery' on GitHub by visiting:
remote:      https://github.com/damusey/Assignment-1/pull/new/Delivery
remote:
To https://github.com/damusey/Assignment-1.git
 * [new branch]      Delivery -> Delivery
------------------------------------------------------------------------------------------
(v)
E:\ps\Assignment-1>git checkout Feature
Switched to branch 'Feature'

E:\ps\Assignment-1>echo "temporary file" >> tmp.file

E:\ps\Assignment-1>git add .

E:\ps\Assignment-1>mkdir tempF

E:\ps\Assignment-1>cd tempF

E:\ps\Assignment-1\tempF>echo "temp2 file" >> tmp2.txt

E:\ps\Assignment-1\tempF>cd ..

E:\ps\Assignment-1>git status
On branch Feature
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   tmp.file

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        tempF/


E:\ps\Assignment-1>git add .

E:\ps\Assignment-1>git commit -m "Adding tmp.txt and tempF"
[Feature ef65cd6] Adding tmp.txt and tempF
 2 files changed, 2 insertions(+)
 create mode 100644 tempF/tmp2.txt
 create mode 100644 tmp.file
---------------------------------------------------------------------------------
(vi)
E:\ps\Assignment-1>git push
fatal: The current branch Feature has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin Feature


E:\ps\Assignment-1>git push origin Feature
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (5/5), 401 bytes | 401.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/damusey/Assignment-1.git
   4d41724..ef65cd6  Feature -> Feature
----------------------------------------------------------------------------------
(viii)
E:\ps\Assignment-1>git checkout master
Switched to branch 'master'

E:\ps\Assignment-1>git pull origin master
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 631 bytes | 17.00 KiB/s, done.
From https://github.com/damusey/Assignment-1
 * branch            master     -> FETCH_HEAD
   4d41724..cb74e49  master     -> origin/master
Updating 4d41724..cb74e49
Fast-forward
 tempF/tmp2.txt | 1 +
 tmp.file       | 1 +
 2 files changed, 2 insertions(+)
 create mode 100644 tempF/tmp2.txt
 create mode 100644 tmp.file
-------------------------------------------------------------------------------------
(ix)Pull merges the files requested from a branch of remote repository
to the branch of local repository while checkout is used to switch
between different branches.
-------------------------------------------------------------------------------------

1(c)
(i)
..............SOFT RESET.......................
E:\ps\Assignment-1>git ls-tree -r master
100644 blob dee7ee39e3d40c3eecb44f115504b007ed8f2ae1    bait.txt
100644 blob 52c3cfd9ff74a355c9bee0d06ed625156ca28bbe    file1.txt
100644 blob 29045fb84567fc08116b30a6438bd099fbc3b166    tempF/tmp2.txt
100644 blob 7fc1caf8c0c15132c4e7bec45e7584aa070b75fe    tmp.file

E:\ps\Assignment-1>git log --oneline
6b41dc9 (HEAD -> master) kill
cb74e49 (origin/master) Merge pull request #1 from damusey/Feature
ef65cd6 (origin/Feature, Feature) Adding tmp.txt and tempF
4d41724 (origin/QA, origin/Prod, origin/Dev, origin/Delivery, QA, Prod, Dev, Delivery) 1st commit

E:\ps\Assignment-1>git reset --soft HEAD~1

E:\ps\Assignment-1>git log --oneline
cb74e49 (HEAD -> master, origin/master) Merge pull request #1 from damusey/Feature
ef65cd6 (origin/Feature, Feature) Adding tmp.txt and tempF
4d41724 (origin/QA, origin/Prod, origin/Dev, origin/Delivery, QA, Prod, Dev, Delivery) 1st commit

E:\ps\Assignment-1>git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   bait.txt

...............HARD RESET...............

E:\ps\Assignment-1>git log --oneline
876178a (HEAD -> master) 2nd bait for Hard
cb74e49 (origin/master) Merge pull request #1 from damusey/Feature
ef65cd6 (origin/Feature, Feature) Adding tmp.txt and tempF
4d41724 (origin/QA, origin/Prod, origin/Dev, origin/Delivery, QA, Prod, Dev, Delivery) 1st commit

E:\ps\Assignment-1>git reset --hard HEAD~1
HEAD is now at cb74e49 Merge pull request #1 from damusey/Feature

E:\ps\Assignment-1>git log --oneline
cb74e49 (HEAD -> master, origin/master) Merge pull request #1 from damusey/Feature
ef65cd6 (origin/Feature, Feature) Adding tmp.txt and tempF
4d41724 (origin/QA, origin/Prod, origin/Dev, origin/Delivery, QA, Prod, Dev, Delivery) 1st commit
----------------------------------------------------------------------------------------------------
