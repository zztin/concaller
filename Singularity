BootStrap: debootstrap
OSVersion: xenial
MirrorURL: http://us.archive.ubuntu.com/ubuntu/


%runscript
    /root/TideHunter/bin/TideHunter ./test_data/test_1000x10.fa > cons.fa
%labels
   AUTHOR l.t.chen-4@umcutrecht.nl
%post
    # pre-build preparation
    apt-get update
    apt-get -y install python3 git wget build-essential libz-dev
    # begin to build TideHunter
    wget https://github.com/yangao07/TideHunter/releases/download/v1.2.2/TideHunter-v1.2.2.tar.gz
    tar -zxvf TideHunter-v1.2.2.tar.gz
    cd TideHunter-v1.2.2; make
    pwd
