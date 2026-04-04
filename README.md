# TP-Link Firmware Update Portal

This repository contains a professional simulation of a TP-Link firmware update portal, designed for authorized network security testing, research, and educational purposes.

## Project Structure

The project is organized into a clean, modular structure:

- `templates/`: Contains localized HTML templates for the portal.
  - `pt-BR/`: Brazilian Portuguese version.
  - `en-US/`: English (US) version.
- `assets/`: Shared resources used by all templates.
  - `css/`: Stylesheets (Bootstrap and custom styles).
  - `js/`: JavaScript libraries (jQuery, Popper, Bootstrap).
  - `img/`: Images and brand logos.
- `eaphammer/`: Integrated EAPHammer tool for deployment (included for convenience).
- `venv/`: Python virtual environment with all necessary dependencies for EAPHammer.

## Deployment with EAPHammer

This project is pre-configured to work seamlessly with EAPHammer as a captive portal module.

### Installation

1. Ensure all dependencies are installed (see `eaphammer/README.md`).
2. The custom portal modules are already linked in:
   `eaphammer/core/wskeyloggerd/templates/user_defined/`

### Running the Portal

To launch the portal, use the following commands from the project root:

**Portuguese Version:**
```bash
sudo ./venv/bin/python3 eaphammer/eaphammer -i <interface> --essid "TP-Link_Update" --captive-portal --portal-template tplink-portal-pt-br
```

**English Version:**
```bash
sudo ./venv/bin/python3 eaphammer/eaphammer -i <interface> --essid "TP-Link_Update" --captive-portal --portal-template tplink-portal-en-us
```

## Legal Disclaimer

This project is intended for authorized security testing and educational use only. Unauthorized use against networks without explicit permission is illegal and unethical. The authors assume no liability for misuse of this software.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
