# W7_BabySoC_Physical_Design

**OpenROAD + noVNC Cloud Environment**
This repository launches a **ready-to-use GitHub Codespace** with OpenROAD tools, an XFCE desktop, and browser-based **noVNC** access.  
It is designed for testing and learning **physical design (PD) flows** in a cloud-based environment — without needing any local installation.

---
## 🚀 Launch the Codespace

1. Click **Code → Codespaces → Create codespace on main**
  ![Launch Codespace]<img width="645" height="581" alt="image" src="https://github.com/user-attachments/assets/7d132733-bb55-46d0-9333-135bb219ade4" />



2. Wait for the setup to complete.  
   The log will show: **“Finished configuring codespace.”**  
   ![Codespace Log] <img width="973" height="99" alt="image" src="https://github.com/user-attachments/assets/403a6bd6-ba57-4f85-8d74-5ca0513851d4" />

   ![Codespace Created]<img width="1023" height="148" alt="image" src="https://github.com/user-attachments/assets/4165780f-7119-48ca-b6d0-498149a2b6c9" />
---

##  Run OpenROAD Flow Scripts
   
Once inside the Codespace terminal (or through the noVNC desktop terminal):

```bash
cd ~/Desktop
git clone https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts.git
cd OpenROAD-flow-scripts/flow
make
````

When the process finishes successfully, you’ll see a log summary similar to this:
![Flow Complete]<img width="966" height="238" alt="image" src="https://github.com/user-attachments/assets/1b61d93b-258b-4bac-9a9b-9b40bd94a526" />
<img width="875" height="613" alt="image" src="https://github.com/user-attachments/assets/20711244-5143-448e-930f-1143d7e7c186" />

## Access the GUI via noVNC

1. Open the **PORTS** tab in the Codespace.
2. Click the 🌐 icon next to **port 6080** to open the noVNC desktop.
   ![Open VNC]<img width="1670" height="319" alt="image" src="https://github.com/user-attachments/assets/c43fb369-e517-4db2-9e3c-a4dbd0b04756" />

You’ll see the browser-based desktop environment:
![VNC Lite]<img width="397" height="317" alt="image" src="https://github.com/user-attachments/assets/e6b8ee9d-db76-4fe6-a251-d3a5736fb462" />

---

## View the Final Layout in GUI
Inside the noVNC desktop terminal, launch the final GUI view:
```bash
cd OpenROAD-flow-scripts/flow
make gui_final
```
![Open VNC]
![Open VNC]<img width="1449" height="811" alt="image" src="https://github.com/user-attachments/assets/ddb27f7f-9ed0-418a-907f-e0323f8963e1" />


## ⚠️ Important Notice

This Codespace setup uses the official
👉 [**OpenROAD Flow Scripts**](https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts)
from the **OpenROAD Project**.

It is intended **only for educational and testing purposes** as part of the **VSD Cloud Codespace Environment**.
For official documentation, updates, and support, please refer to the OpenROAD repository linked above.

















