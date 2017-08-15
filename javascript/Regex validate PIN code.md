# Regex validate PIN code

ATM machines allow 4 or 6 digit PIN codes and PIN codes cannot contain anything but exactly 4 digits or exactly 6 digits.
If the function is passed a valid PIN string, return true, else return false.

### Examples:

  - validatePIN("1234") === true
  -  validatePIN("12345") === false
  -  validatePIN("a234") === false

### Solution

>function validatePIN (pin) {
>
>  var patt=new RegExp(/^\d{4}(\d{2})?$/);
>
>return patt.test(pin);
>
>}
