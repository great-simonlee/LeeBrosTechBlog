---
layout: post
title: New MacBook Setting
categories: devenv setting
author: Simon Lee
permalink: /:categories/:title
---

<strong>>> [NOMAD YouTube Video for a New MacBook Setting][nomad] <<</strong>
<strong>>> [Homebrew Official Website][homebrew] <<</strong>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 32px; font-weight: bold; margin-bottom: 18px; padding-top: 32px; border-top: black solid 1px;">1. Homebrew</div>
<strong>!!! DO NOT FORGET TO FOLLOW THE "Next steps" SECTION !!!</strong>
<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Restart the terminal</div>
<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Run "brew" to see if it works</div>
<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Run the following code snippet</div>
{% highlight c %}
brew install --cask visual-studio-code google-chrome slack iterm2
{% endhighlight %}

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 32px; font-weight: bold; margin-bottom: 18px; padding-top: 32px; border-top: black solid 1px;">2. Iterm Config</div>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Preferences > Appearance > General > Theme: Refular -> Minimal</div>
<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Preferences > Profiles > Session: Check "Status bar enabled" and click the config btn</div>
<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Move what you want to add and Change the color to "Light Colors"</div>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 32px; font-weight: bold; margin-bottom: 18px; padding-top: 32px; border-top: black solid 1px;">2. Iterm Color Theme</div>

<strong>>> [Iterm2 Color Schemes][itermcolor] <<</strong>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Choose the color and download it (Right click and save as..)</div>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Remove the txt extension and run it (I chose GitHub Dark)</div>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Preferences > Colors > Color Presets: Choose what you downloaded</div>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 32px; font-weight: bold; margin-bottom: 18px; padding-top: 32px; border-top: black solid 1px;">3. Oh My Zsh</div>

<strong>>> [Oh My Zsh Official Website][ohmyzsh] <<</strong>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Install Oh My Zsh with command line code</div>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 32px; font-weight: bold; margin-bottom: 18px; padding-top: 32px; border-top: black solid 1px;">4. Power Level 10k</div>

<strong>>> [Power Level 10k Github Page][powerlevel10k] <<</strong>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Installation > Oh My Zsh: Copy and paste the commnand line code</div>

{% highlight c %}
code ~/.zshrc
{% endhighlight %}

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Change ZSH_THEME="robbyrussell" to ZSH_THEME="powerlevel10k/powerlevel10k"</div>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Quit the iterm and restart it</div>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">PowerLever10k Config will pop up automatically and select the followings</div>

<p style="font-family: 'Times New Roman', serif; font-size: 16px">1-1) Font: y</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">1-2) Restart the iterm</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">2) Check: yyyy</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">3) Style: 32323421n1y</p>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 32px; font-weight: bold; margin-bottom: 18px; padding-top: 32px; border-top: black solid 1px;">5. Dev Tools</div>

{% highlight c %}
brew install python3 pipenv nvm gh
{% endhighlight %}

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">#1 Node Version Manager (NVM): You should export the PATH under the last line of code in the <strong>CONFIGURATION FILE</strong></div>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">1) Open the config file</p>

{% highlight c %}
code ~/.zshrc
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px">2) Copy the following code snippet and paste under the last line of code in the config file</p>

{% highlight c %}
export NVM_DIR="$HOME/.nvm"
[ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && \. "/opt/homebrew/opt/nvm/nvm.sh" # This loads nvm
[ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" # This loads nvm bash_completion
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px">3) Restart the iterm</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">4) Run the following line of code to check if nvm works</p>

{% highlight c %}
nvm ls-remote
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px">5) Install the latest version of nvm by runnning the following code</p>

{% highlight c %}
nvm install 17.5.0
node -v
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px">6) Install the (Latest LTS: Gallium) version of nvm by runnning the following code</p>

{% highlight c %}
nvm install 16.14.0
nvm use 17.5.0
nvm use 16.14.0
{% endhighlight %}

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">#2 Github</div>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">1) Run the following line of code</p>

{% highlight c %}
gh auth login
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px">2) Select GitHub.com</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">3) Select HTTPS</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">4) Yes</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">5) Login with a web browser</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">6) Copy one-time code and activate it</p>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 32px; font-weight: bold; margin-bottom: 18px; padding-top: 32px; border-top: black solid 1px;">6. Visual Studio</div>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">#1 Extensions</div>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">1) GitLens</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">2) Material Icon Theme</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">3) Community Material Theme</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">4) Bracket Pair Colorizer 2</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">5) CSS Peek</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">6) ESLint</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">7) HTML CSS Support</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">8) indent-raindow</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">9) Live Server</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">10) Prettier</p>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">#2 Setting</div>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">VS Settings > Search "terminal font"</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px">Type "MesloLGS NF" in the blank box of 'Terminal > Integrated: Font Family'</p>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 32px; font-weight: bold; margin-bottom: 18px; padding-top: 32px; border-top: black solid 1px;">7. MacBook M1 Chip Laptop: Activate Rosetta</div>

{% highlight c %}
/usr/sbin/softwareupdate --install-rosetta --agree-to-license
{% endhighlight %}

<br>
<br>
<br>

[nomad]: https://www.youtube.com/watch?v=B26yiuC5zPM&list=WL&index=1
[homebrew]: https://brew.sh/
[itermcolor]: https://iterm2colorschemes.com/
[ohmyzsh]: https://ohmyz.sh/
[powerlevel10k]: https://github.com/romkatv/powerlevel10k
