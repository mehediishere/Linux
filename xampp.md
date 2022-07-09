<p align="center"> <code> XAMPP INSTALLATION PROCESS </code> </p>
<p align="center">
  <a href="https://www.apachefriends.org/index.html" target="_blank">
    <img src="https://managewp.com/wp-content/uploads/2012/08/xampp-logo.png" width="400">
  </a>
</p>

## Change the permissions to the installer

```
chmod 755 xampp-linux-*-installer.run
```

## Run the installer

```
sudo ./xampp-linux-*-installer.run
```
That's all. XAMPP is now installed below the /opt/lampp directory.

## To start XAMPP simply call this command:

```
sudo /opt/lampp/lampp start
```
Also, note that there is a graphical tool that you can use to manage your servers easily. You can start this tool with the following commands:

```
cd /opt/lampp
```
```
sudo ./manager-linux.run (or manager-linux-x64.run)
```

## To stop XAMPP simply call this command:

```
sudo /opt/lampp/lampp stop
```

## How to create Xampp shortcut in Ubuntu's/Other Distro's Start Menu

Firstly, cd to/usr/share/applications
```
cd /usr/share/applications
```

Then create a new file with extension is *.desktop by opening the terminal then run this command:

```
sudo touch xampp.desktop
```

Open the new file with super admin right by:

```
sudo gedit xampp.desktop
```

Paste following to the file content:

```
[Desktop Entry]
Encoding=UTF-8
Name=XAMPP Control Panel
Comment=Start and Stop XAMPP
Exec=sudo /opt/lampp/manager-linux-x64.run
Icon=/opt/lampp/htdocs/favicon.ico
Categories=Application
Type=Application
Terminal=true
```
<code>Exec:</code> Command to run the application (with Xampp you need <code>sudo</code> right).
<code>Terminal: true</code> if you want to open terminal when running this application. With Xampp I set value is <code>true</code> to type the password of <code>sudo</code> when running the app.

Save the file, now you have the Xampp shortcut available on start menu.

Credit (Xampp's Shortcut):
[Truong An](https://www.dinorunn.com/how-to-create-xampp-shortcut-in-ubuntu-start-menu/)
<br>
Reference: [XAMPP FAQs](https://www.apachefriends.org/faq_linux.html)
