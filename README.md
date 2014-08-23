gg-uncrustify-config
====================

My version of config file for uncrustify for Objective C code.


How to install and start using Uncrustify
=========================================

1. Install brew 
	ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)”

2. Install brew completion
	brew install bash-completion git
 
3. Install uncrustify
	brew install uncrustify

4. Download Xcode plugin from
	https://github.com/benoitsan/BBUncrustifyPlugin-Xcode

5. Place downloaded file in ~/Library/Application Support/Developer/Shared/Xcode/Plug-ins

6. Copy uncrustify-GG.cfg to your home directory and rename it to uncrustify.cfg

7. Restart Xcode and see under Edit menu the newly added option to execute.



Batch run uncrustify on all source files
========================================

1. Open Terminal and goto source directory. Rrun following command. Here dot is for current directory.
	find . -name '*.m' > list.txt

2. Then run following command, assuming that uncrustify.cfg is placed in your home directory
	uncrustify -c ~/uncrustify.cfg --replace -F list.txt

