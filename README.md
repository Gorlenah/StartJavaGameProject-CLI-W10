# StartJavaGameProject-CLI-W10
Instructions to start POLIMI Project on W10 with WSL &amp; Windows Terminal

Main Guide: [Tutor Bertoni Guide](https://github.com/michele-bertoni/W10JavaCLI)

This guide was inspired by the tutor's guide

1. ## Download & install Font:
	* DejaVu Sans Mono for Powerline.ttf - [LINK](https://github.com/Gorlenah/StartJavaGameProject-CLI-W10/blob/master/font/DejaVu%20Sans%20Mono%20for%20Powerline.ttf)

2. ## Install Bash on Ubuntu on Windows (BUW)
	* Open Windows PowerShell as Administrator by pressing ```WINDOWS + X``` and then selecting the correct voice
	* Enable the "Windows subsystem for Linux" by running ```Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux```
	* Reboot when asked
	* Install [Ubuntu from Microsoft Store](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
	* Launch the application and set username and password
  
3. ## Install Java on (BUW)
  	* ```sudo apt update```
  	* ```sudo add-apt-repository ppa:linuxuprising/java```
  	* ```sudo apt -y install oracle-java14-installer```
  	<br>[Source](https://computingforgeeks.com/how-to-install-java-14-on-ubuntu-debian/)
  
4. ## Now you can run your jar on BUW
  	* ```cd path/to/jar/```
  	* ```java -jar fileName.jar```
  
5. ## You can Run also on Windows Terminal:
  	* Install [Windows Terminal](https://github.com/microsoft/terminal/releases) (assets file.msixbundle)
	or [MS-Store](https://www.microsoft.com/store/productId/9N0DX20HK701)
  
  	* Launch It & go to setting (settings.json appears)
  	* Search ```"name": "Ubuntu"``` in ```"list":``` (if ubuntu doesn't appear do this steps)<br>
		* Find ```"list":```<br>
    
		* Add at the end of List Array:
		    ```
		    {
			"guid": "{2c4de342-38b7-51cf-b940-2309a097f518}",
			"hidden": false,
			"name": "Ubuntu",
			"source": "Windows.Terminal.Wsl",
			"startingDirectory": "%USERPROFILE%/Desktop"
		    }
		    ```
      
  	* N.B: With ```"startingDirectory": "%USERPROFILE%/Desktop"``` you can choose the default starting directory of BUW
  	* Set: ``` "defaultProfile":"{2c4de342-38b7-51cf-b940-2309a097f518}", ``` (with same guid of ubuntu if you want it as default console)
	* Set: Defaults Settings to change font, or add ```"fontFace"``` & ```"fontSize"``` to your favorite guid
	```
        "defaults":
        {
            // Put settings here that you want to apply to all profiles.
		"fontFace": "DejaVu Sans Mono for Powerline",
           	"fontSize": 12
        },
	```

* N.B: You can copy settings.json present in this repo
* N.B: After launching Windows Terminal, you can press F11 to view the console in full screen
