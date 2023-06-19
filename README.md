<div align="center">
  <h1>Check store version</h1>
  
  <p> a simple package for react native </> 
  <p> that checks the app version in the stores and returns the response of the comparison </>
  <p> between the local version and the store version.</>
</div>

<div align="center">
  
</div>

<br>
<br>

>Status: Developing ⚠️

## 💻 Getting started

### Requirements

- The app must already be published.
- Need to specify bundleIndentfier and buildNumber in app.json file.

### Installing

 ```npm i check-store-version```

### Using

```javascript
import checkVersion from "check-store-version";
```
checkVersion is an asynchronous function that receives as a parameter the app's id on the Google Play Store, the app's id on the App Store, and the location (example: 'us', 'br'...)
```javascript
const verifyUpdateStore = async () => {
    try {
      const check = await checkVersion(
        "br.com.company.app",
        "1213478177",
        "br"
      );
      console.log(check);
      if (check.result === "new") {
      }
    } catch (e) {}
  };
```
The function returns an object with the following properties:
- local (local version).
- remote (remote version).
- result ('new' or 'old').
- detail ('remote > local', 'remote < local', 'remote === local').
<br>

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

<hr>
<div align="center">
  <sub>Copyright Â© 2023-present, DouglasNeves.</sub>
</div>
<hr>
