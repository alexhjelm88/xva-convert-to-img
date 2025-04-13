XVA to IMG Converter

A simple Python script to convert XCP-ng or XenServer .xva virtual machine backups into .img files, making them compatible for import into Proxmox VE or other hypervisors.

🚀 Features

Converts .xva files exported from XCP-ng or XenServer to .img disk images.

Supports importing converted .img files directly into Proxmox or other hypervisor platforms.

Automatically handles gaps and zero-fills missing blocks, ensuring proper image integrity.

📦 Requirements

Python 3.x (tested on Python 3.8+)

🔧 Installation & Usage

Clone the repository:

git clone https://github.com/yourusername/xva-to-img-converter.git
cd xva-to-img-converter

Run the script:

python3 xva_to_img.py yourfile.xva

This generates one or more .img files:

yourfile.xva-0.img
yourfile.xva-1.img
...

📌 Example: Importing to Proxmox

To import a converted image into Proxmox VE:

qm importdisk <vmid> yourfile.xva-0.img local-lvm

Replace <vmid> with the VM ID in Proxmox, and local-lvm with your storage name.

⚠️ Error Handling

The script provides clear error messages for common issues:

Non-existent input files.

Output file already existing.

Invalid or corrupted TAR files.

📄 License

MIT License - Feel free to modify and share.

🤝 Contributions

Contributions are welcome! Open a pull request or issue if you encounter bugs or have suggestions for improvement.

© 2025 Alexander Hjelm

