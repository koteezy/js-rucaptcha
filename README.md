# ruCaptcha

# ruCaptcha
Little wrapper for rucaptcha API

## Create instance
```
const rc := ruCaptcha.create({
    key: null, // Required: Your api key.
    in: 1, // Not required|Default: http://rucaptcha.com/in.php
    res: 1, // Not required|Default: http://rucaptcha.com/res.php
    delay: 1000, // Not required|Default: 1000
    debug: false, // Not required|Default: false
})
 
or
 
new ruCaptcha({...})
```
## Solve a google recaptcha
```
try {
   const captcha = await rc.google('google site key', 'page url')
} catch (err) => {
    console.log(err.toString());
}
 
or
  
rc.google('google site key', 'page url')
.then(captcha => {...})
.catch(err => {...})
```