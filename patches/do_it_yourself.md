# If you want to build your own cgminer with patches:

git clone https://github.com/ckolivas/cgminer.git

cd cgminer

git checkout 9afd0a216a0f95adb650e4818f24af1a61ad837d

This will give you original cgminer 4.6.1 from ckolivas source

then download patches:
-
for BTC hexminer:

wget https://raw.githubusercontent.com/wareck/cgminer-hexminer/master/patches/rev_9afd0a216a0f95adb650e4818f24af1a61ad837d.patch

for Scrypt Hexminer:

wget https://raw.githubusercontent.com/wareck/cgminer-hexminer/master/patches/srev_9afd0a216a0f95adb650e4818f24af1a61ad837d.patch

for both (extranonce optimisation from nicehash):

wget https://raw.githubusercontent.com/wareck/cgminer-hexminer/master/patches/extranonce-patch.patch

if you want to use Hexminer BTC:

patch -p1 <rev_9afd0a216a0f95adb650e4818f24af1a61ad837d.patch

if you want to use Hexminer Scrypt:

patch -p1 <srev_9afd0a216a0f95adb650e4818f24af1a61ad837d.patch

if you want add extranonce options (nicehash special optminisation):

patch -p1 <extranonce-patch.patch


Compilation:
-

for BTC Hexminer:

./autogen.sh --enable-hexminera --enable-hexminerb  --enable-hexmineru --enable-hexminerc  --enable-hexminer8 --enable-hexminerm --enable-hexminerr --enable-hexminerbe200 --enable-hexminer3 

./configure --enable-hexminera --enable-hexminerb  --enable-hexmineru --enable-hexminerc  --enable-hexminer8 --enable-hexminerm --enable-hexminerr --enable-hexminerbe200 --enable-hexminer3 

make

for Scrypt Hexminer:

./autogen.sh --enable-hexminers

./configure --enable-hexminers

make

