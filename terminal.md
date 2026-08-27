- [cheatsheet for the zsh basics](https://media.datacamp.com/legacy/image/upload/v1700048361/Bash_Cheat_Sheet_4503e68287.png)
- [cheatsheet for mac terminal basics (with some extra zsh stuff already covered in the zsh cheatsheet)](https://imgv2-1-f.scribdassets.com/img/document/431102014/original/6092b3e1f9/1?v=1)  
  
Something that's not obvious from the get-go is that there are actually two pieces to it: the terminal and the shell. We use the words interchangeably and to mean the combination of the two (especially "terminal").  
- The shell is the thing that actually runs commands
    - zsh is default on mac. powershell or cmd on windows.
- The terminal is the thing that creates the window the shell runs in and has hotkeys, tabs, and themes.
  
There's a lot of value in customizing the terminal and shell. A lot of it requires time spent learning how and why. Some easier first steps might be:
- Setting your terminal font to something readable.
    - [This website](https://www.programmingfonts.org/) lets you test drive a bunch of different fonts and then you can go figure out how to install it :)
    - You can also set the font in your IDE to match
- Setting the terminal theme & opacity
    - Not quite sure how to do it on mac terminal or if it includes any by default but there's [plenty on the web](https://github.com/lysyi3m/macos-terminal-themes)
- [Add some aliases](https://stackoverflow.com/questions/73254636/how-do-you-set-an-alias-in-zsh-on-macos) in `~/.zshrc` for everyday workflow stuff
    - e.g.  `gl` for `git pull` and `gp` for `git push`

And then a bit higher on the tree there's:  
- Customizing zsh
    - You can go with a kitchen sink approach like [zsh-quickstart-kit](https://github.com/unixorn/zsh-quickstart-kit) or build stuff up from scratch in your `~/.zshrc` file with something like [Oh My Zsh](https://ohmyz.sh/)
        - zqs is a bit overwhelming at first and has some implications for how you configure zsh after using it, but I like it quite a bit.
- Managing your dotfiles (config files that are named something like .zshrc) with git or chezmoi.
    - This lets you track your configuration and makes it easier to deploy on other machines or recover from accidents.
    - I like [chezmoi](https://www.chezmoi.io/) but it's a bit hard to grok if you don't already understand a bit about how your shell works