# StartJavaGameProject-CLI-W10
Instructions to start POLIMI Project on W10 with WSL &amp; Windows Terminal

1. ## Download & install Font:
	* DejaVu Sans Mono for Powerline.ttf

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
