# 🚀 GLPI Docker Container

This repository provides a ready-to-use Docker setup for deploying [GLPI (Gestionnaire Libre de Parc Informatique)](https://glpi-project.org/), an open-source IT Asset Management and Service Desk platform.

The setup includes:
- Automatic download and installation of the latest GLPI version (or a specified one)
- Apache with PHP 8.1 support
- LDAP configuration fix
- Timezone setup
- Cron job for background GLPI tasks

---

## 📦 Features

- ✅ Automatically fetches the **latest GLPI release** from GitHub
- 🌐 Configures **Apache VirtualHost** depending on GLPI version
- 🕒 Sets PHP timezone via environment variable
- 🔁 Adds a **cron job** to run GLPI's scheduled tasks
- 🔧 Includes **rewrite module** for cleaner URLs
- 🛠 Ensures GLPI is installed only if not already present
- 🔐 Adjusts `ldap.conf` to avoid TLS certificate issues

---

## 🧰 Requirements

- Docker Engine ≥ 20.10
- Docker Compose (optional, if using a stack)

---

## 🚀 How to Run

### 🐳 Using Docker

1. Clone the repository:

```bash
git clone https://github.com/cynegeirus/docker-glpi
cd docker-glpi
```

2. Build the image:

```bash
docker-compose build
```

3. Run the container:

```bash
docker-compose up -d
```

## 🌍 Environment Variables

| Variable      | Default         | Description                                  |
|---------------|-----------------|----------------------------------------------|
| `TIMEZONE`    | `Europe/Istanbul` | Timezone applied to PHP config               |
| `VERSION_GLPI`| *latest*        | Specific version tag from GitHub releases    |

---

## License

This project is licensed under the [MIT License](LICENSE). See the license file for details.

---

## Issues, Feature Requests or Support

Please use the Issue > New Issue button to submit issues, feature requests or support issues directly to me. You can also send an e-mail to akin.bicer@outlook.com.tr.
