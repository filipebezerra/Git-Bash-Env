# Git-Bash-Env
Customized configuration for Git Bash such as auto completion, custom colors and editor integration with Sublime Text.

## Getting started
You can follow the instructions below or you can watch the explanatory video from Youtube. If you are using Windows environment then go to [this video][7] or if you are using Linux or Mac environment then go to [this video][8]:

1. Save [this file][1] in your home directory with the name `git-completion.bash`.
2. Save [this file][2] in your home directory with the name `git-prompt.sh`.
3. Save [this file][3] in your home directory with the name `.bash_profile`. If 
you already have a file in your home directory named `.bash_profile`, copy the 
content from [this file][3] and paste it at the bottom of your existing `.bash_profile`.
4. If you're curious to learn more about how bash prompts work, see [this page][4].

## Make sure you can start your editor from Git Bash/terminal
If you use Sublime, you can do this by adding the following line to your `.bash_profile`:

For Windows environment use:
```
alias subl="C:/Program\ Files/Sublime\ Text\ 2/sublime_text.exe"
```
For Mac environment use:
```
alias subl="/Applications/Sublime\ Text\ 2.app/Contents/SharedSupport/bin/subl"
```
For Linux environment use:
```
alias subl="/opt/Sublime\ Text\ 2/sublime_text"
```

## Making Git configurations
Run the following Git configuration commands. The first one will need to be modified if you are using a text editor other than Sublime, or if Sublime is installed in another location for you. See [this page][5] for the correct command for a couple of other popular text editors. For any other editor, you'll need to enter the command you use to launch that editor from Git Bash.

For Windows environment use:
```
git config --global core.editor "'C:/Program Files/Sublime Text 2/sublime_text.exe' -n -w"
```
For Mac environment use:
```
git config --global core.editor "'/Applications/Sublime Text 2.app/Contents/SharedSupport/bin/subl' -n -w"
```
For Linux environment use:
```
git config --global core.editor "'/opt/Sublime Text 2/sublime_text' -n -w"
```

> In the command above, the `-n` parameter means to Sublime open in a new window and `-w` parameter means Git will wait you to close Sublime before try to continue.

The final steps for any environment:
```
git config --global push.default upstream
git config --global merge.conflictstyle diff3
```

>Instead of the first command, you may be able to use the simpler git config --global core.editor "subl -n -w" as shown in the video, but many Udacity students have found this does not work for them.

## Restart Git Bash/terminal
You'll need to close and re-open Git Bash/terminal before all your changes take effect.

## Udacity references
* [Setting Up Your Workspace on Windows - How to Use Git and GitHub][6]
* [Setting Up Your Workspace on Mac - How to Use Git and GitHub][11]

## Sublime Text installation help
* [How to install Sublime Text 2 on Ubuntu 12.04 (Unity)][9]
* [Sublime Text 3 installation - Unofficial documentation][10]

[1]: git-completion.bash
[2]: git-prompt.sh
[3]: .bash_profile
[4]: http://www.cyberciti.biz/tips/howto-linux-unix-bash-shell-setup-prompt.html
[5]: https://help.github.com/articles/associating-text-editors-with-git/
[6]: https://www.udacity.com/course/viewer#!/c-ud775/l-2980038599/m-3341718587
[7]: https://www.youtube.com/watch?v=IfLhXM4RnB4
[8]: https://www.youtube.com/watch?t=15&v=s_eFuGauy6k
[9]: http://www.technoreply.com/how-to-install-sublime-text-2-on-ubuntu-12-04-unity/
[10]: http://sublime-text-unofficial-documentation.readthedocs.org/en/latest/getting_started/install.html
[11]: https://www.udacity.com/course/viewer#!/c-ud775/l-2980038599/m-3333158951
