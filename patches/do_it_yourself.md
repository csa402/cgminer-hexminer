if you want to build your own cgminer with patches:

git clone https://github.com/ckolivas/cgminer.git
cd cgminer
git checkout 9afd0a216a0f95adb650e4818f24af1a61ad837d  // cgminer 4.6.1 
wget https://raw.githubusercontent.com/wareck/cgminer-hexminer/master/patches/rev_9afd0a216a0f95adb650e4818f24af1a61ad837d.patch //original patch from Hexminer
wget https://raw.githubusercontent.com/wareck/cgminer-hexminer/master/patches/srev_9afd0a216a0f95adb650e4818f24af1a61ad837d.patch //original patch from Herminer scrypt

if you want to use Hexminer BTC
patch -p1 <rev_9afd0a216a0f95adb650e4818f24af1a61ad837d.patch

if you want to use Hexminer Scrypt
patch -p1 <srev_9afd0a216a0f95adb650e4818f24af1a61ad837d.patch


