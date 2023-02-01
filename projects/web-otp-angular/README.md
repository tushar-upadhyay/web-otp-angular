
# web-otp-angular

Angular library to automatically detect OTP from mobile device (Both mobile web site and Desktop)





## Installation

`npm i web-otp-angular`

Add `WebOtpAngularModule` to imports in your `app.module.ts` file.

## Usage
Just add directive `appWebOtp` in your `<input>` tag where you want to autofill the otp value.

```html
<div>
    <h2>Example of code</h2>
    <input appWebOtp  type="number" placeholder="Your OTP" />
<div>
```

## Optional

add `[timeout]` property to abort listening for the OTP (in milliseconds)

Below example will stop listening to the otp after 5 seconds.

```html
   <input appWebOtp [timeout]="5000" type="number" placeholder="Your OTP" />
```



## OTP SMS Format

You must use following SMS format to detect the OTP.

```
Your OTP is: 123456.

@www.yourwebsite.com #123456

```
Checkout more on https://web.dev/web-otp/