---
layout: post
title:  "Customize your shell with 'oh my zsh' and autojump "
date:   2016-04-09
categories: shell
permalink: /category/shell/customize
---

1. install iterm
2. install autojump:

	
	> brew install autojump
	

3. install oh my zsh
	

	> sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

	above will install oh my zsh to your local. It will change your default shell to zsh at the end of the process, if it doesn’t, execute below:

	> chsh -s /bin/zsh

4. Open .zshrc file which located at the root of current user. e.g. /Users/joezhang/
5. Modify `plugin` to include “autojump”, like `plugins=(git,autojump)`
6. Add this into the .zshrc file 

	> [[ -s $(brew --prefix)/etc/profile.d/autojump.sh ]] && . $(brew --prefix)/etc/profile.d/autojump.sh
