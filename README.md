# git-recipes-DaichiMatsu
エンピット

Part A

A1. 

ファイル数

git-recipes-DaichiMatsu　% find .git/objects -type f | wc -l     

       2

ファイル数がゼロでない理由

git-recipes-DaichiMatsu　% ls -a

              .		..		.git		README.md

上の実行結果からも分かる通り、git-recipes-DaichiMatsuの中には".git"と"README.md"の二つのファイルが存在するから
