# My Powershell settup

PreRequires:-   
	git  
	gcc or gnu (compilers)  
	Windows Terminal  
	Powershell  
	Scoop  				

## Install the Hack Nerd Font
	* Simple open ttf file and click install * 
## Windows Terminal Settings

```
	enable arylic material in the tab row tab
	set font to HACK NF font
	set colorscheme to One Dark
```
## Install powershell from Store

```
	change default to Powershell
	open settings.json 
	copy the whole one dark theme
	and paste it and change name some-else
	now change background #001B26
	and now change appreance themes to some-else

```

## Install Scoop

```
	Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
	irm get.scoop.sh | iex
```

```
	scoop install curl sudo jq
```

```
	curl 'https://api.inkdrop.app/' | jq
```

## Setting up powershell user profile

	* Make powershell dir in .config  *
	* And create a file in powershell dir named as user_profile.ps1  *
	* Copy these lines to user_profile.ps1 *
	
	
	```
	.# Alias
	Set-Alias vim nvim
	Set-Alias ll ls
	Set-Alias g git
	Set-Alias grep findstr
	Set-Alias tig 'C:\Program Files\Git\usr\bin\tig.exe'
	Set-Alias less 'C:\Program Files\Git\usr\bin\less.exe'
	
	```
	*and now edit this file  *  
	* if not create a directory in document names PowerShell and a file called Microsoft.PowerShell_profile.ps1  *  
	
	* nvim $PROFILE.CurrentUserCurrentHost *  
	*paste this line  *
	
	
	```
		. $env:USERPROFILE\.config\powershell\user_profile.ps1
	```

## Installing post and setting up
```
	Install-Module posh-git -Scope CurrentUser -Force
```


```
	Install-Module oh-my-posh -Scope CurrentUser -Force
```

	*and again open user_profile.ps1 and add these to top of the file*
	```
	#Prompt
	Import-Module posh-git
	Import-Module oh-my-posh
	Set-PostPrompt Parado
	```

	*If got any error please install this directly*
	```
		Set-ExecutionPolicy Bypass -Scope Process -Force; Invoke-Expression ((New-Object System.Net.WebClient).DownloadString('https://ohmyposh.dev/install.ps1'))
	```
