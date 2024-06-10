# Planetary Dials 🌍

Planetary Dials is a utility library for mapping country codes, dial codes, and their flags.

## Installation

To install this library, you can use the following command:

```bash
npm install --save @erboladaiorg/distinctio-voluptates-officia
```

## Usage

Here's an example of how you can use this library in your code:

```typescript
import {
    Country,
    getPlanetaryDials,
    getCountryDialCode,
    getCountryFlag,
    getCountryName
} from "@erboladaiorg/distinctio-voluptates-officia";

// all countries

console.log(getPlanetaryDials());
/*
{
  AF: {
    flag: 'https://flagsapi.com/AF/shiny/64.png',
    code: 'AF',
    name: 'Afghanistan',
    dialCode: '+93'
  },
  AX: {
    flag: 'https://flagsapi.com/AX/shiny/64.png',
    code: 'AX',
    name: 'Aland Islands',
    dialCode: '+358'
  },
  ...
}
*/


// one country
console.log(getCountryDialCode(Country.AF));
// +93

console.log(getCountryFlag(Country.AF));
// https://flagsapi.com/AF/shiny/64.png

console.log(getCountryName(Country.AF));
// Afghanistan


// multiple countries
const countryCodes: Country[] = [Country.US, Country.CA];
const result = getMultipleCountryDialInfo(countryCodes);
console.log(result);
/*
[
  {
    flag: 'https://flagsapi.com/US/shiny/64.png',
    code: 'US',
    name: 'United States',
    dialCode: '+1'
  },
  {
    flag: 'https://flagsapi.com/CA/shiny/64.png',
    code: 'CA',
    name: 'Canada',
    dialCode: '+1'
  }
]
*/
```

## Contributing

Contributions to this project are welcome. Please open an issue or pull request on GitHub.

## License

This project is licensed under the ISC license.

This library is inspired by [michaelolof's country-flags-dial-codes](https://github.com/michaelolof/country-flags-dial-codes)".