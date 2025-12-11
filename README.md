# Atlas

Based on **Sixty's Atlas Auto Installer** - Downloads and installs kiwix, VLC, and jDownloader

> Sixty's original script also downloads Ollama and MSTY, but I am not using any LLMs in my setup (at this time).

## About the script

1. Update the OS:
```bash
sudo apt update && sudo apt upgrade
```
2. Create a directory in Documents labeled “Kiwix-zims”
```bash
mkdir -p "${HOME}/Documents/Kiwix-zims"
```
3. Create a TXT file on the desktop labeled “Quick Links” and put the following information inside: 
> “Download zims from here: library.kiwix.org
> 
> Download websites and turn them into zims here: zimit.kiwix.org/
> 
> When downloading zims, place them into the Kiwix-zims folder in your Documents”
4. Open port 8080 using ufw
```bash
ufw --force enable
ufw allow 8080/tcp
```
> Consider adjusting this step if using a different firewall.

> The original script downloads ollama and msty. These will be omitted.
```bash
# Omit these
curl -fsSL https://ollama.com/install.sh | sh
ollama pull qwen2.5:0.5b
https://assets.msty.app/prod/latest/linux/amd64/Msty_amd64_amd64.deb
sudo apt install ./<DownloadedFileName>.deb
# Create a shortcut to run “msty” on the Desktop
```
5. Install vlc, kiwix, and jDownloader.
```bash
sudo apt install vlc kiwix snapd core jdownloader2 -y
```

## Additional Links

### Zims

Download zims from [here](library.kiwix.org).

Download websites and turn them into zims [here](zimit.kiwix.org/).

#### Instructions

1. Download zims to your directory.
  a. Alternatively, convert your desired websites into zims.
2. Open Kiwix, Select "..." > **Settings** > **Browse** > **Documents** > **Kiwix-zims** > OK

Now Kiwix will look at that directory for any new zim's you add!



# Reference

## Overview - Install - Setup:

[YouTube Link](https://www.youtube.com/watch?v=L5RJZmuRJKA)
