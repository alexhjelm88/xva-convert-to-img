# XVA to IMG Converter

A simple Python script to convert XCP-ng or XenServer `.xva` virtual machine backups into `.img` files, suitable for import into Proxmox VE or other hypervisors.

## ✨ Features

- Converts `.xva` files exported from XCP-ng or XenServer into `.img` disk images.
- Ready-to-use `.img` files compatible with Proxmox and similar hypervisors.
- Automatically fills gaps with zeros, ensuring disk image integrity.

## 📌 Requirements

- Python 3.x (tested on Python 3.8+)

## 🚀 Installation & Usage

1. Clone the repository:

   git clone https://github.com/alexhjelm88/xva-convert-to-img.git
   cd xva-convert-to-img

2. Run the script:

   python3 xva-convert-to-img.py yourfile.xva

### Output

The script generates `.img` files, such as:

- `yourfile.xva-0.img`
- `yourfile.xva-1.img`

## 🔧 Example: Importing to Proxmox

To import your converted disk image into Proxmox VE:

qm importdisk <vmid> yourfile.xva-0.img local-lvm

- Replace `<vmid>` with your Proxmox VM ID.
- Replace `local-lvm` with your Proxmox storage name.

## ⚠️ Error Handling

The script clearly communicates issues, including:

- Missing input files.
- Output file already exists.
- Invalid or corrupted TAR files.

## 📜 License

Released under the [MIT License](LICENSE). Feel free to modify, distribute, and use freely.

## 🤝 Contributions

We welcome contributions! Submit a pull request or create an issue for bugs, suggestions, or enhancements.

---

© 2025 Alexander Hjelm
