# Mac Python Install (Work in Progress)

I recently installed a brand new mac with Mojave and started using pyenv. 

First install brew.

```
xcode-select --install
install -pkg /Library/Developer/CommandLineTools/Packages/macOS_SDK_headers_for_macOS_10.14.pkg
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Then install **pyenv**. And the most important versions.

```
brew install pyenv
pyenv install 3.6    # shows 3.6.6 is latest
pyenv install 3.6.6 
pyenv install 3.7    # shows 3.7.0 is latest
pyenv install 3.7.0
pyenv versions       # shows installed versions
```

Now update your profile, **~/.bash_profile** or **~/.zshrc**, and add:

```
export PATH=$PATH:~/.local/bin/
eval "$(pyenv init -)"
```

Set global python to 3.7.0.

```
python --version
pyenv global 3.7.0
```

Open a new terminal and install the awscli.

```
pip install awscli
```

Test if it works.

```
aws --version
```

# Install zsh

Probably this will be another manual, but for now it's a short addition.

```
brew install zsh zsh-completions
curl -L https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh | sh
chsh -s /bin/zsh
```

