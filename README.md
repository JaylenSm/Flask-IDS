# Flask-IDS
This is a lightweight, IDS pipeline utilized with a dashboard script to dynamically and safely display threat logs treated as text. So code in logs can not be executed by the Flask interpreter. Jinja2 is used to accomplish this as it escapes HTML logic. The IDS is standalone without any other solutions put in place, however, an IPS is simulated via the blocking of access to the admin page. Which is set to serve the "403" forbidden page by default when showcasing the project. Due to an IDS and IPS solution typically being served together. 

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

## 📜 Table of Contents

- [Features](#Features)
- [Usage](#Usage)
- [Presentation](#Presentation)
- [Requirements](#Requirements)
- [Installation](#Installation)

# Features 

- The package features a Docker-ready IDS prototype pipeline stack, complete with a Flask web-server that leverages Jinja2, a dashboard with it's own dedicated environment, and an IDS engine whose I/O operations communicate with the dashboard.

- As the web service is essentially a honeypot the IDS engine is strongly configured to detect injection-based attacks in an input parameter on a form.

- The package includes a dockerfile that allows for quick, portable image and container building.

# Usage

The intended usage of this package is to demonstrate to employers the functionality of my project. It is not intended for personal or commercial benefit, however, the codebase is open to researchers who wish to reference my model. Although, optimability shouldn't be expected as this is a logical demonstration. 

# Presentation

For a presentation/demo of the project [CLICK ME](https://onedrive.live.com/:p:/g/personal/8D3E98D829540707/ESvu3V1S6vJGjr9dlvnkVU0BGHtKPD3NyqD_e2FWwZP65Q?resid=8D3E98D829540707!s5dddee2bea5246f28ebf5d96f9e4554d&ithint=file%2Cpptx&e=okM3HH&migratedtospo=true&redeem=aHR0cHM6Ly8xZHJ2Lm1zL3AvYy84ZDNlOThkODI5NTQwNzA3L0VTdnUzVjFTNnZKR2pyOWRsdm5rVlUwQkdIdEtQRDNOeXFEX2UyRld3WlA2NVE_ZT1va00zSEg).

# Requirements

- To run this project have Docker installed.

- Have the flask library installed (The requirements.txt file lists flask which will automatically be installed by the Dockerfile.).

- Have Python3 (3.10-slim installed by Dockerfile) installed in your working environment.

# Installation

- Install the appropriate package listed in this repo.

- Extract the package.

- Open a terminal in the package folder.

- Type and execute the command "docker build --no-cache -t <DESIRED_IMAGE_NAME> ."

- Type and execute the command "docker run --name <DESIRED_CONTAINER_NAME> -p 5000:5000 <CREATED_IMAGE_NAME>"

- You can now access the honeypot via localhost/127.0.0.1 address and port 5000!

