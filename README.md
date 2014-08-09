passwordManager
===============

A password system that stores data locally, stores a key file externally, and has a management interface for when your device is stolen.

Hard requirements:
- Requests password once per login session. Restoring from lock screen should request the master password again.
- Each time a password is used, the server side key file should be requested.
- The server will only serve the key-file to pre-approved devices, controlled through the web interface.
- No password information should be recorded server side, only the login information for the site, the key file, the device name. To request the file, it should be the username and device name.
- NB. It is important that the local master password and server account passwords are different. Still, the device will need to be physically accessible. Foreign devices will not have the local data required to get keys.
- NB. This won't be fool proof. If someone gets the password, local access, and packet sniffs the server key file, and then redirects locally for the software to look locally for the key file. There may be some public key thing that can be done to protect against this though.

Fluffy requirements:
- Chrome, Firefox, Android, iPhone integration. Preferably some sort of semi-auto insertion of information in to webforms. This will hopefully be fine, but there might need to be some metainformation particular to each OS. Ie... if the field names served up are different, the user will have to be able to direct the software to the password field.
- Best to have a fairly light but attractive windows interfacce. And Mac, I guess... It should be controllable completely from the app.
- Needs to packaged all together. KeePass looks gross, and trying to instal it is a nightmare, since it is all plugins that have unclear dependencies, and are a nightmare to debug when they don't work. Impossible to a lay-person.

Similar projects:
- LastPass - paid service that stores passwords in the cloud
- KeePass - a nice open project that relies on independently written extensions
- Norton Something something. Looks good, but it is a standard Norton calamity.
