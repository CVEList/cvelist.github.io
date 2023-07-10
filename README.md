# risksDrivers - Living Off The Land Drivers 🚗💨

![CI build](https://github.com/boss-net/risksDrivers/actions/workflows/validate.yml/badge.svg)

Welcome to risksDrivers (Living Off The Land Drivers), an exciting open-source project that brings together vulnerable, malicious, and known malicious Windows drivers in one comprehensive repository. Our mission is to empower organizations of all sizes with the knowledge and tools to understand and address driver-related security risks, making their systems safer and more reliable.

## Key Features

- An extensive and well-organized collection of vulnerable and malicious Windows drivers
- Continuously updated with the latest information on driver vulnerabilities and threats
- Easy-to-navigate categories and indices for quick access to relevant information
- Seamless integration with Sigma for proactive defense using hash prevention

## How risksDrivers Can Help Your Organization

- Enhance visibility into vulnerable drivers within your infrastructure, fostering a stronger security posture
- Stay ahead of the curve by being informed about the latest driver-related threats and vulnerabilities
- Swiftly identify and address risks associated with driver vulnerabilities, minimizing potential damages
- Leverage compatibility with Sigma to proactively block known malicious drivers by hash

## Getting Started

To begin your journey with risksDrivers, simply check out the [risksDrivers.io](https://boss-net.github.io/risksdrivers/) site or clone the repository and explore the wealth of information available in the categorized directories. We've designed the site to help you easily find the insights you need to protect your systems from vulnerable drivers.

To assist in speeding up the creating of a yaml file, check out [risksdrivers.streamlit.app](https://risksdrivers.streamlit.app)

## Support 📞

Please use the [GitHub issue tracker](https://github.com/boss-net/risksDrivers/issues) to submit bugs or request features.

## 🤝 Contributing & Making PRs

Stay engaged with the risksDrivers community by regularly checking for updates and contributing to the project. Your involvement will help ensure the project remains up-to-date and even more valuable to others.

Join us in our quest to create a safer and more secure digital environment for organizations everywhere. With risksDrivers by your side, you'll be well-equipped to tackle driver-related security risks and confidently navigate the ever-evolving cyber landscape.

If you'd like to contribute, please follow these steps:

1. Fork the repository
2. Create a new branch for your changes
3. Make your changes and commit them to your branch
4. Push your changes to your fork
5. Open a Pull Request (PR) against the upstream repository

For more detailed instructions, please refer to the [CONTRIBUTING.md](CONTRIBUTING.md) file. To create a new YAML file for a driver, use the provided [YML-Template](YML-Template.yml).

## 🚨 Sigma and Sysmon Detection

risksDrivers provides comprehensive Sigma and Sysmon detection rules to help you effectively detect potential threats. To explore these rules in detail, navigate to the [sigma](detections/sigma/) and [sysmon](detections/sysmon/) directories under the detection folder.

Happy hunting! 🕵️‍♂️

## 🔎 Windows Folder Scanning

The community has also created a PowerShell LOLDriver scanner courtesy of [@Oddvarmoe](https://twitter.com/Oddvarmoe), [@M_haggis](https://twitter.com/M_haggis), and [IISResetMe](https://twitter.com/IISResetMe), that can help you identify potentially malicious drivers. The script, available [here](https://gist.github.com/IISResetMe/1a8353ae57710868b31b0e8d41683b95), allows you to scan a specified Windows folder for any suspicious files. We recommend running the script on directories such as:

```
C:\WINDOWS\inf
C:\WINDOWS\System32\drivers
C:\WINDOWS\System32\DriverStore\FileRepository
```

## 🏗️ Building and Testing Locally

### Requirements

* [Python 3.10](https://www.python.org/downloads/)
* [Poetry](https://python-poetry.org/docs/#installation)
* [Golang](https://go.dev/dl/)
* [Hugo](https://gohugo.io/)

### Steps to Build and Test Locally

1. Clone the repository:

```
git clone https://github.com/boss-net/risksDrivers.git
```

2. Change to the project directory:

```
cd risksDrivers
```

3. Install dependencies:

```
poetry install
```

4. Activate the virtual environment:

```
poetry shell
```

5. Build the site using the files under the /yaml folder:

```
python bin/site.py
```

6. Run the website locally:

```
cd boss-net.github.io/risksdrivers && hugo serve
```
