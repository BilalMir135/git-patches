# git patch

git patch help us to achieve a scenario in which we want to move one branch few commits to another branch instead of moving complete code.

Like in this example I want to move **feat:03** code from `feature` branch to `main`. But feature branch have code of upto **feat:05**.

## Steps

1. In branch `feature` check the commits you have upto **feat:03** for that run _git log_.
2. In this example we have 3 commits ahead of main feat:01,02 and then feat 03 so inorder to move **feat:03** to main we have to move all these commits patches.
3. To create patches for all these commits run **git format-patch -3 [commit-hash of feat:03] -o patches**, this will create 3 patches file inside patches directory.
4. Checkout to `main` branch and run **git apply patches/\***, this will apply all patches present in patches directory with sequence.
