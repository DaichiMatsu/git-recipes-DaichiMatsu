# git-recipes-DaichiMatsu
エンピット

Part A

A1. 

ファイル数:

(base) daichi.matsumoto@matsumotodaichinoMacBook-Air git-recipes-DaichiMatsu % find .git/objects -type f | wc -l         

       2

上の実行結果よりファイル数は2

ファイル数がゼロでない理由:

(base) daichi.matsumoto@matsumotodaichinoMacBook-Air git-recipes-DaichiMatsu % ls -a

       .		..		.git		README.md

上の実行結果からも分かる通り、git-recipes-DaichiMatsuの中には".git"と"README.md"の二つのファイルが存在するから


A2.

(base) daichi.matsumoto@matsumotodaichinoMacBook-Air git-recipes-DaichiMatsu % cat .git/HEAD && cat .git/refs/heads/kitchen/DaichiMatsu    

       # .git/HEADの中身
       ref: refs/heads/kitchen/DaichiMatsu

       # ブランチのファイルの中身
       1a1135b781f06b66049169b3ea2ce55a739c01a3


A3.

(base) daichi.matsumoto@matsumotodaichinoMacBook-Air git-recipes-DaichiMatsu % git cat-file -p HEAD^{tree}

       # treeにはREADME.mdファイルのみが並んでいる
       100644 blob a6823fc44dcc90b4c8cd22c58dc96cbe47bc0675	README.md


A4.

(base) daichi.matsumoto@matsumotodaichinoMacBook-Air git-recipes-DaichiMatsu % git log --oneline | tail -1

       1a1135b Initial commit

(base) daichi.matsumoto@matsumotodaichinoMacBook-Air git-recipes-DaichiMatsu % git checkout 1a1135b && cat .git/HEAD
Note: switching to '1a1135b'.

       You are in 'detached HEAD' state. You can look around, make experimental
       changes and commit them, and you can discard any commits you make in this
       state without impacting any branches by switching back to a branch.

       If you want to create a new branch to retain commits you create, you may
       do so (now or later) by using -c with the switch command. Example:

         git switch -c <new-branch-name>

       Or undo this operation with:

         git switch -

       Turn off this advice by setting config variable advice.detachedHead to false

       HEAD is now at 1a1135b Initial commit
       
       1a1135b781f06b66049169b3ea2ce55a739c01a3

(base) daichi.matsumoto@matsumotodaichinoMacBook-Air git-recipes-DaichiMatsu % git checkout -b rescue && git checkout kitchen/DaichiMatsu && git branch -d rescue

       Switched to a new branch 'rescue'
       Switched to branch 'kitchen/DaichiMatsu'
       Deleted branch rescue (was 1a1135b).



Part B

(base) daichi.matsumoto@matsumotodaichinoMacBook-Air git-recipes-DaichiMatsu % git log --oneline -n 4

       e1bd5d0 (HEAD -> kitchen/DaichiMatsu) final2
       de43a10 oops
       3162239 fix
       ebf14b0 aaa
