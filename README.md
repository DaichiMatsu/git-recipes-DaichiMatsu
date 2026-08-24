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

       ref: refs/heads/kitchen/DaichiMatsu

       1a1135b781f06b66049169b3ea2ce55a739c01a3
