# ruCaptcha

# ruCaptcha
Little wrapper for rucaptcha API

## Create instance
```
const rc = ruCaptcha.create({
    key: null, // Required: Your api key.
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

##Solve a google recaptcha v3
```
try {
   const captcha = await rc.google('google site key', 'page url', {
    user_score: '0.4',
    version: 'v3'
   })
} catch (err) => {
    console.log(err.toString());
}
```