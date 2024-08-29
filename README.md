# Telegram Account Age Estimator

A simple Node.js utility that estimates the registration date of a Telegram account based on its numeric ID. This tool provides the approximate month and year of registration, along with the number of years since the account was created.

## Features

- **Approximate Registration Date**: Get a rough estimate of the month and year when the account was created.
- **Account Age**: Calculate how many years have passed since the account was registered.
- **Boundary Handling**: The tool handles cases where the provided ID is older or newer than the known range of data.

## Installation

First, clone the repository and navigate to the project directory:

```bash
git clone https://github.com/yourusername/telegram-account-age-estimator.git
cd telegram-account-age-estimator
```

Then, install the required dependencies:

```bash
npm install
```

## Usage

To use the tool, simply require the module and pass a Telegram account ID to the `getAge` function. 

```javascript
const getAge = require('./getAge');

const id = 12345678; // Replace with the Telegram account ID you want to estimate
const [ageStatus, approxDate, yearsSince] = getAge(id);

console.log(`Status: ${ageStatus}`);
console.log(`Approximate Registration Date: ${approxDate}`);
console.log(`Years Since Registration: ${yearsSince}`);
```

### Sample Output

```bash
Status: aprox
Approximate Registration Date: 5/2015
Years Since Registration: 9
```

## Data Source

The tool uses a JSON file (`ages.json`) that contains a mapping of known Telegram IDs to their respective registration timestamps. This data is used to interpolate and estimate the registration date for any given ID.

## Contributing

Contributions are welcome! If you find a bug or have a feature request, please open an issue or submit a pull request.

This README provides a clear explanation of what the tool does, how to install and use it, and how others can contribute. The project title and description give a concise overview of the utility's purpose and functionality.
