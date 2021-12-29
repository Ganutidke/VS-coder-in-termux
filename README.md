# VS-coder-in-termux
Run VS coder IDE on android using termux 


How to install VS Code in an Android Phone?



In this post, we will see how you can install vs code on an android device. We will use one of the most popular android terminals called termux.

Follow the steps below:

Step 1 - Install termux

In order to install VS code, you will have to install termux using this link. The official release available on the play store doesn't seem to get the packages updated for some reason.

If upgrade command doesn't work on your termux, try to change the default repo by using the command below:

termux-change-repo

Step 2 - Install ubuntu using termux

Enter the following command on termux and ubuntu will start to install on your Android phone

pkg install wget openssl-tool proot -y && hash -r && wget https://raw.githubusercontent.com/EXALAB/AnLinux-Resources/master/Scripts/Installer/Ubuntu/ubuntu.sh && bash ubuntu.sh

start ubuntu by firing the following command:

./start-ubuntu.sh

Step 3 - Downloading code server

We will now download the latest release of code server from Github using the following command:

wget https://github.com/cdr/code-server/releases/download/v3.10.2/code-server-3.10.2-linux-arm64.tar.gz

Extract the tarball using the following command:

tar -xvf ./code-server-3.10.2-linux-arm64.tar.gz

enter the /bin folder of your code-server installation on ubuntu (running on your phone)

cd code-server-3.10.2-linux-arm64

cd bin

Step 4 - Set up a password and start using VS Code

Setup a password for your VS Code instance using the following command:

export PASSWORD="password"

Launch the code server using the following command:

code-server
