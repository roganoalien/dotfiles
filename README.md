## Where and how
The `.zshrc` file goes inside `./~` folder after `iterm2` and `ohmyzsh` are installed.

###### Theme
This file refers to `ZSH_THEME="agnoster"`theme which needs the file to be installed in the same `./~` folder.

###### Plugins
`zsh-iterm-touchbar` for the usage of ZSH funcionalities in the macos touchbar

###### Print some text when a neew window or tab is open
Needs the global installation of `fortune` and `cowsay` and the function is `fortune | cowsay -f stegosaurus`

###### Custom function to make directory and cd inside of it
The shortcut before the folder name is: `mkcd`

```shell
function mkcd(){
  mkdir $1 && cd $1
}
```

###### Aliases
There are a lot of alias for tree functionality, cd to default repositories folder to run mongo, open file or folder in sublime text and connect to some servers.

###### Autosuggestions
`source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh` this needs the file for the plugin and this `ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE='fg=magenta'` changes the color of the autosuggestions from the default console profile colors

###### PATHS
The path configuration for mongodb, android studio and deno

###### Random emoji on new window or tab
The next function selects a random emoji from a bunch and prints it before thee user and folder directory. Needs a fix cause sometimes shows an empty emoji

```shell
emojis=("🦖" "🦕" "👺" "🎄" "🌵" "🌙" "⚡️" )
EMOJI=${emojis[$RANDOM % ${#emojis[@]} ]}

prompt_context() {
	printf " ${EMOJI} ";
}
```
