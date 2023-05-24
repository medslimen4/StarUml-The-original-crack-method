# StarUml-The-original-crack-method

StarUML . The original crack method, how to modify the license verification function 
cannot be used. The installation location has changed and the LicenseManagerDomain.js file has been found. 
What should I do? The old driver told everyone to solve the problem.

StarUML is written in nodejs. Specifically, it is written on the front frame of Electron. 
All starUML source code in the new version is packaged by the roasting tool. 

# go to the directory (Windows)

C:\Program Files\StarUML\resources

# install the tool asar

```bash
npm install -g asar
```

# unpack StarUML use the command:

```bash
asar extract app.asar app
```
# Edit the license file :

```bash
app\src\engine\license-manager.js
```

### modify the code
line 125

```js
  checkLicenseValidity () {
    this.validate().then(() => {
      setStatus(this, true)
    }, () => {
    //===> Cambiar false por true
      setStatus(this, true)
      //===> Comentar Dialog
      // UnregisteredDialog.showDialog()
    })
  }
```

# repackage StarUML use  the command :

```bash
  asar pack app app.asar
 ```
 
 # execute StarUML
 
  
