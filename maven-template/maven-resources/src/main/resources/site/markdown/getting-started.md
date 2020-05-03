## Getting Started

### Git
1. Download and install [Git SCM](https://git-scm.com/downloads).
2. Open **Git Bash**.
3. Setup Git global config
	```bash
	git config --global user.name "Full Name"
	git config --global user.email "Full.Name@domain.com"
	git config --global core.autocrlf true
	```
---

### Maven
1. Download [Apache Maven](http://maven.apache.org/download.cgi).
2. Extract the downloaded zip into **D:\Maven** (or any folder).
3. Create directory junction for .m2 folder, so any downloaded artifact will be stored in **D:\Maven\repository**.
	```bash
	mklink /J %userprofile%\.m2 D:\Maven
	```
4. Setup M2_HOME environment variable.
	- Go to **Windows Button -> Search "edit environment variables for your account"**.
	- On new window, click **New...**
		```properties
		Variable name=M2_HOME
		Variable value=D:\Maven\apache-maven
		```
	- Select **Path**, then click **Edit...**.
	- Click **New**, then put **%M2_HOME%\bin**.
---

### Eclipse JEE IDE
- Download [Eclipse JEE IDE](https://www.eclipse.org/downloads/packages).

#### Setup Lombok
1. Download [lombok.jar](https://projectlombok.org/download).
2. Double click the jar, the installer window should appear.
3. Click **Specify location...**, then browse your **eclipse.exe** file.
4. Click **Install / Update**, it will install the library to your Eclipse IDE.
5. Click **Quit Installer**.

For more information about lombok setup, visit https://projectlombok.org/setup/eclipse.