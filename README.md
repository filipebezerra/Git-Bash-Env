# Git-Bash-Env
Customized configuration for Git Bash such as auto completion, custom colors and editor integration with Sublime Text.

## Windows Configuration
### Getting started
1. Save [this file][1] in your home directory with the name `git-completion.bash`.
2. Save [this file][2] in your home directory with the name `git-prompt.sh`.
3. Save [this file][3] in your home directory with the name `.bash_profile`. If 
you already have a file in your home directory named `.bash_profile`, copy the 
content from [this file][3] and paste it at the bottom of your existing `.bash_profile`.
4. If you're curious to learn more about how bash prompts work, see [this page][4].

### Making Git configurations
Run the following Git configuration commands. The first one will need to be modified if you are using a text editor other than Sublime, or if Sublime is installed in another location for you. See [this page][5] for the correct command for a couple of other popular text editors. For any other editor, you'll need to enter the command you use to launch that editor from Git Bash.
```
git config --global core.editor "'C:/Program Files/Sublime Text 2/sublime_text.exe' -n -w"
git config --global push.default upstream
git config --global merge.conflictstyle diff3
```

### Make sure you can start your editor from Git Bash
If you use Sublime, you can do this by adding the following line to your `.bash_profile`:
```
alias subl="C:/Program\ Files/Sublime\ Text\ 2/sublime_text.exe"
```

## Restart Git Bash
You'll need to close and re-open Git Bash before all your changes take effect.

## Reference
* [How to Use Git and GitHub - Udacity course][6]

[1]: git-completion.bash
[2]: git-prompt.sh
[3]: .bash_profile
[4]: http://www.cyberciti.biz/tips/howto-linux-unix-bash-shell-setup-prompt.html
[5]: https://help.github.com/articles/associating-text-editors-with-git/
[6]: https://www.udacity.com/course/viewer#!/c-ud775/l-2980038599/m-3341718587


