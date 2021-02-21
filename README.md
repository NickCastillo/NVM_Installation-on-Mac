# 🛠 NVM (Node Version Manager) installation on MacOS with zsh:
As it turns out, NVM isn't compatible with homebrew, this is stated on the [official nvm-sh repo](https://github.com/nvm-sh/nvm#installation-and-update). You can find the installation guide there as well, however, long story short:

+ `brew uninstall nvm` (just in case)

+ `brew cleanup` (As a good practice, do this at your own risk though🥴)

+ `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.36.0/install.sh | bash` (This installs nvm or, if you already have it, upgrades it)

+ Now let's see if it was installed correctly: `command -v nvm`

If you get "nvm" as a result, you are good to go!🙌🏼🎉 

If you did not get "nvm", running the following lines worked for me (and I hope it works for you too 🥺). 

`export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" `

## Now to finish up:

+ `nvm install-latest-npm` (this updates your Node.js)
+ `nvm install --lts` (this updates npm)
