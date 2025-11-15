# W7_BabySoC_Physical_Design

**OpenROAD + noVNC Cloud Environment**
This repository launches a **ready-to-use GitHub Codespace** with OpenROAD tools, an XFCE desktop, and browser-based **noVNC** access.  
It is designed for testing and learning **physical design (PD) flows** in a cloud-based environment — without needing any local installation.

---
### What It Is

This repository provides a cloud-based environment (like GitHub Codespaces or VSCode in the browser) that runs:

OpenROAD tools – used for ASIC physical design automation (placement, routing, timing, etc.)

XFCE Desktop – a lightweight Linux desktop environment

noVNC – a browser-based remote desktop viewer

So, instead of installing OpenROAD locally, you can run and view it directly in your browser.
###  Why It’s Useful

✅ No need to install OpenROAD or GUI tools locally
✅ Works directly in your browser
✅ Ideal for learning and experimenting with ASIC design flow
✅ Perfect for education, workshops, or testing small designs

## 🚀 Launch the Codespace

A Codespace is a personal cloud-based development environment provided by GitHub.
Think of it as your own mini Linux computer running in the cloud, automatically created for a specific repository.

1. Go to this repository in your browser:
 ```  bash
🔗 https://github.com/vsdip/vsd-pd
```
2. Click **Code → Codespaces → Create codespace on main**
   
When you open the repository in GitHub → click “Code → Open with Codespaces → New codespace”.
GitHub spins up a virtual machine (VM) in the cloud, running Ubuntu or Debian.

This VM includes:
All required tools (like OpenROAD, Yosys, Magic, KLayout)
A Linux desktop environment (XFCE)
noVNC server setup for browser-based GUI access
 
  <img width="645" height="581" alt="image" src="https://github.com/user-attachments/assets/7d132733-bb55-46d0-9333-135bb219ade4" />

2. Wait for the setup to complete.  
   The log will show: **“Finished configuring codespace.”**  
   <img width="973" height="99" alt="image" src="https://github.com/user-attachments/assets/403a6bd6-ba57-4f85-8d74-5ca0513851d4" />

  <img width="1023" height="148" alt="image" src="https://github.com/user-attachments/assets/4165780f-7119-48ca-b6d0-498149a2b6c9" />


##  Run OpenROAD Flow Scripts
   **Installing and setting up ORFS**
Once inside the Codespace terminal (or through the noVNC desktop terminal):

```bash
cd ~/Desktop
git clone https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts.git
cd OpenROAD-flow-scripts/flow
make
````
This downloads and runs the official OpenROAD physical design flow (synthesis → placement → routing).

⏳ This process can take 10–20 minutes depending on system size.

When the process finishes successfully, you’ll see a log summary similar to this:
<img width="966" height="238" alt="image" src="https://github.com/user-attachments/assets/1b61d93b-258b-4bac-9a9b-9b40bd94a526" />
<img width="875" height="613" alt="image" src="https://github.com/user-attachments/assets/20711244-5143-448e-930f-1143d7e7c186" />

## Access the GUI via noVNC

1. Open the **PORTS** tab in the Codespace.
2. Click the 🌐 icon next to **port 6080** to open the noVNC desktop.
   → This opens a new browser tab showing the XFCE desktop using noVNC.
  You’ll now see a Linux desktop GUI inside your browser!
```bash
# 🌐 Accessing the GUI (Port 6080)
# Use the following URL format to open the VNC GUI in your browser:
# 6080 → open in browser
# https://yourusername-vsd-pd-xxxx-6080.app.github.dev/vnc.html
#
# Replace:
#   yourusername → your GitHub username
#   xxxx → the unique Codespace ID
```
    <img width="1670" height="319" alt="image" src="https://github.com/user-attachments/assets/c43fb369-e517-4db2-9e3c-a4dbd0b04756" />

You’ll see the browser-based desktop environment:
<img width="397" height="317" alt="image" src="https://github.com/user-attachments/assets/e6b8ee9d-db76-4fe6-a251-d3a5736fb462" />

---

## View the Final Layout in GUI
Inside the noVNC desktop terminal, launch the final GUI view:
```bash
cd OpenROAD-flow-scripts/flow
make gui_final
```
This launches the OpenROAD GUI where you can view your chip layout and final routing results.

<img width="1486" height="717" alt="Screenshot (441)" src="https://github.com/user-attachments/assets/80daccfa-809b-4bb0-abe4-a89fd7b9ea38" />

<img width="1783" height="922" alt="Screenshot (444)" src="https://github.com/user-attachments/assets/502842bd-b5c7-449f-bc7b-3128ea9c5703" />

<img width="1753" height="853" alt="Screenshot (446)" src="https://github.com/user-attachments/assets/6cb50f8e-73c6-4935-8d61-79f52ceec1d3" />




### ⚠️ Notes

- Everything runs in the cloud — **no installation is required on your PC**.  
- All files, logs, and intermediate outputs are **saved automatically inside your Codespace**.  
- If you close the Codespace, you can **reopen it anytime** as long as it has not been deleted.

## ⚠️ Important Notice

This Codespace setup uses the official
👉 [**OpenROAD Flow Scripts**](https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts)
from the **OpenROAD Project**.

It is intended **only for educational and testing purposes** as part of the **VSD Cloud Codespace Environment**.
For official documentation, updates, and support, please refer to the OpenROAD repository linked above.


# PHYSICAL DESIGN OF BABYSOC

**ORFS Directory Structure and File formats**

``` 
├── OpenROAD-flow-scripts             
│   ├── docker           -> It has Docker based installation, run scripts and all saved here
│   ├── docs             -> Documentation for OpenROAD or its flow scripts.  
│   ├── flow             -> Files related to run RTL to GDS flow  
|   ├── jenkins          -> It contains the regression test designed for each build update
│   ├── tools            -> It contains all the required tools to run RTL to GDS flow
│   ├── etc              -> Has the dependency installer script and other things
│   ├── setup_env.sh     -> Its the source file to source all our OpenROAD rules to run the RTL to GDS flow
```

Now, go to flow directory

``` 
├── flow           
│   ├── design           -> It has built-in examples from RTL to GDS flow across different technology nodes
│   ├── makefile         -> The automated flow runs through makefile setup
│   ├── platform         -> It has different technology note libraries, lef files, GDS etc 
|   ├── tutorials        
│   ├── util            
│   ├── scripts             
```

<img width="1866" height="251" alt="Screenshot (447)" src="https://github.com/user-attachments/assets/cf292d2c-2912-4fc8-9924-4f0c3ec3ca41" />

### Automated RTL2GDS Flow for VSDBabySoC:

Initial Steps:

- We need to create a directory `vsdbabysoc` inside `OpenROAD-flow-scripts/flow/designs/sky130hd`
- Now create a directory `vsdbabysoc` inside `OpenROAD-flow-scripts/flow/designs/src` and include all the verilog files here.
- Now copy the folders `gds`, `include`, `lef` and `lib` from the VSDBabySoC folder in your system into this directory.
  - The `gds` folder would contain the files `avsddac.gds` and `avsdpll.gds`
  - The `include` folder would contain the files `sandpiper.vh`, `sandpiper_gen.vh`, `sp_default.vh` and `sp_verilog.vh`
  - The `gds` folder would contain the files `avsddac.lef` and `avsdpll.lef`
  - The `lib` folder would contain the files `avsddac.lib` and `avsdpll.lib`
- Now copy the constraints file(`vsdbabysoc_synthesis.sdc`) from the VSDBabySoC folder in your system into this directory.
- Now copy the files(`macro.cfg` and `pin_order.cfg`) from the VSDBabySoC folder in your system into this directory.

 ```bash
    OpenROAD-flow-scripts/
 └── flow/
     └── designs/
         ├── sky130hd/
         │    └── vsdbabysoc/
         └── src/
              └── vsdbabysoc/
     ```


Step1-
```bash
cd ~/Desktop
git clone https://github.com/your-username/VSDBabySoC.git
```
    
```bash
     cp -r VSDBabySoC/gds OpenROAD-flow-scripts/flow/designs/sky130hd/vsdbabysoc/
     cp -r VSDBabySoC/include OpenROAD-flow-scripts/flow/designs/sky130hd/vsdbabysoc/
     cp -r VSDBabySoC/lef OpenROAD-flow-scripts/flow/designs/sky130hd/vsdbabysoc/
     cp -r VSDBabySoC/lib OpenROAD-flow-scripts/flow/designs/sky130hd/vsdbabysoc/
     cp VSDBabySoC/vsdbabysoc_synthesis.sdc OpenROAD-flow scripts/flow/designs/sky130hd/vsdbabysoc/
     cp VSDBabySoC/macro.cfg OpenROAD-flow-scripts/flow/designs/sky130hd/vsdbabysoc/
     cp VSDBabySoC/pin_order.cfg OpenROAD-flow-scripts/flow/designs/sky130hd/vsdbabysoc/
     cp -r VSDBabySoC/src OpenROAD-flow-scripts/flow/designs/src/vsdbabysoc/
 ```
### So By Absolute Paths
```bash
cp -r ~/Desktop/VSDBabySoC/src/gds /workspaces/vsd-pd/OpenROAD-flow-scripts/flow/designs/sky130hd/vsdbabysoc/
cp -r ~/Desktop/VSDBabySoC/src/include /workspaces/vsd-pd/OpenROAD-flow-scripts/flow/designs/sky130hd/vsdbabysoc/
cp -r ~/Desktop/VSDBabySoC/src/lef /workspaces/vsd-pd/OpenROAD-flow-scripts/flow/designs/sky130hd/vsdbabysoc/
cp -r ~/Desktop/VSDBabySoC/src/lib /workspaces/vsd-pd/OpenROAD-flow-scripts/flow/designs/sky130hd/vsdbabysoc/
cp -r ~/Desktop/VSDBabySoC/src/layout_conf /workspaces/vsd-pd/OpenROAD-flow-scripts/flow/designs/sky130hd/vsdbabysoc/

cp ~/Desktop/VSDBabySoC/src/sdc/vsdbabysoc_synthesis.sdc /workspaces/vsd-pd/OpenROAD-flow-scripts/flow/designs/sky130hd/vsdbabysoc/
cp ~/Desktop/VSDBabySoC/src/layout_conf/vsdbabysoc/macro.cfg /workspaces/vsd-pd/OpenROAD-flow-scripts/flow/designs/sky130hd/vsdbabysoc/
cp ~/Desktop/VSDBabySoC/src/layout_conf/vsdbabysoc/pin_order.cfg /workspaces/vsd-pd/OpenROAD-flow-scripts/flow/designs/sky130hd/vsdbabysoc/
```
Step2-
- Now, create a `config.mk` file whose contents are shown below:
  
1️⃣ In the Codespaces file explorer (left sidebar), navigate to:
```bash
OpenROAD-flow-scripts
└── flow
└── designs
└── sky130hd
└── vsdbabysoc
```
2️⃣ Inside the **vsdbabysoc** folder, click **“New File”**.

3️⃣ Name the file:

4️⃣ Paste the entire `config.mk` content into this file and save it.


```
export DESIGN_NICKNAME = vsdbabysoc
export DESIGN_NAME = vsdbabysoc
export PLATFORM    = sky130hd

# export VERILOG_FILES_BLACKBOX = $(DESIGN_HOME)/src/$(DESIGN_NICKNAME)/IPs/*.v
# export VERILOG_FILES = $(sort $(wildcard $(DESIGN_HOME)/src/$(DESIGN_NICKNAME)/*.v))
# Explicitly list the Verilog files for synthesis
export VERILOG_FILES = $(DESIGN_HOME)/src/$(DESIGN_NICKNAME)/vsdbabysoc.v \
                       $(DESIGN_HOME)/src/$(DESIGN_NICKNAME)/rvmyth.v \
                       $(DESIGN_HOME)/src/$(DESIGN_NICKNAME)/clk_gate.v

export SDC_FILE      = $(DESIGN_HOME)/$(PLATFORM)/$(DESIGN_NICKNAME)/vsdbabysoc_synthesis.sdc

export vsdbabysoc_DIR = $(DESIGN_HOME)/$(PLATFORM)/$(DESIGN_NICKNAME)

export VERILOG_INCLUDE_DIRS = $(wildcard $(vsdbabysoc_DIR)/include/)
# export SDC_FILE      = $(wildcard $(vsdbabysoc_DIR)/sdc/*.sdc)
export ADDITIONAL_GDS  = $(wildcard $(vsdbabysoc_DIR)/gds/*.gds.gz)
export ADDITIONAL_LEFS  = $(wildcard $(vsdbabysoc_DIR)/lef/*.lef)
export ADDITIONAL_LIBS = $(wildcard $(vsdbabysoc_DIR)/lib/*.lib)
# export PDN_TCL = $(DESIGN_HOME)/$(PLATFORM)/$(DESIGN_NICKNAME)/pdn.tcl

# Clock Configuration (vsdbabysoc specific)
# export CLOCK_PERIOD = 20.0
export CLOCK_PORT = CLK
export CLOCK_NET = $(CLOCK_PORT)

# Floorplanning Configuration (vsdbabysoc specific)
export FP_PIN_ORDER_CFG = $(wildcard $(DESIGN_DIR)/pin_order.cfg)
# export FP_SIZING = absolute

export DIE_AREA   = 0 0 1600 1600
export CORE_AREA  = 20 20 1590 1590

# Placement Configuration (vsdbabysoc specific)
export MACRO_PLACEMENT_CFG = $(wildcard $(DESIGN_DIR)/macro.cfg)
export PLACE_PINS_ARGS = -exclude left:0-600 -exclude left:1000-1600: -exclude right:* -exclude top:* -exclude bottom:*
# export MACRO_PLACEMENT = $(DESIGN_HOME)/$(PLATFORM)/$(DESIGN_NICKNAME)/macro_placement.cfg

export TNS_END_PERCENT = 100
export REMOVE_ABC_BUFFERS = 1

# Magic Tool Configuration
export MAGIC_ZEROIZE_ORIGIN = 0
export MAGIC_EXT_USE_GDS = 1

# CTS tuning
export CTS_BUF_DISTANCE = 600
export SKIP_GATE_CLONING = 1

# export CORE_UTILIZATION=0.1  # Reduce this value to allow more whitespace for routing.
```

<img width="1920" height="825" alt="Screenshot (448)" src="https://github.com/user-attachments/assets/7fe35dba-492e-432f-b186-7fb2da0afafd" />

<img width="1850" height="907" alt="Screenshot (450)" src="https://github.com/user-attachments/assets/abefed0b-6939-4d93-b08a-52daf01efbc7" />

### 📂 Adding VSDBabySoC Verilog Files to OpenROAD
 1. create the following directory inside your Codespace:
```bash
mkdir -p /workspaces/vsd-pd/OpenROAD-flow-scripts/flow/designs/src/vsdbabysoc

```
2️. Copy all Verilog .v files into this new folder
Your original Verilog files are located at:
```bash
~/Desktop/VSDBabySoC/src/vsdbabysoc/
```
Run this command to copy them:
```bash
cp ~/Desktop/VSDBabySoC/src/module/*.v \
/workspaces/vsd-pd/OpenROAD-flow-scripts/flow/designs/src/vsdbabysoc/

```

If you have additional Verilog files in other folders (e.g., rtl/, IP folders), copy them as well.


### Now go to terminal and run the following commands:

```
cd OpenROAD-flow-scripts
source env.sh
cd flow
```
## No need of seperate ' make ' for each flow as this

```
make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.mk synth
```
This error pop ups-
```bash
make: *** No rule to make target 'synth'.  Stop.
```
means your OpenROAD-flow-scripts version does NOT support running make synth directly.
since in Codespaces,

```bash
make
```
This executes the full OpenROAD physical design flow, which includes:

-Logic synthesis (Yosys)
-Floorplanning
-Placement
-Clock tree synthesis
-Routing
-GDSII generation

All of this uses the Nangate45 PDK (Process Design Kit) —
that’s the 45nm open-source standard-cell library used for educational PD flows.

### CORRECT COMMAND IN CODESPACES

```bash
cd /workspaces/vsd-pd/OpenROAD-flow-scripts/flow
make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.mk
```
You can confirm this by 
```bash
grep -i "all:" Makefile
```
You will see something like:
```bash
all: run_flow
```
which explains why default target = full flow.

### ERROR
```bash
 make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.mk
designs/sky130hd/vsdbabysoc/config.mk:11: *** missing separator (did you mean TAB instead of 8 spaces?).  Stop.
```
This error 100% means your config.mk has spaces instead of a TAB on line 11.
Makefiles strictly require TAB before every command.

-Remove all spaces at the beginning
-Use TAB instead.
❌ Wrong (8 spaces)

Here is your fixed, valid OpenLane config.mk (safe version):
```bash
set ::env(DESIGN_NAME) "vsdbabysoc"

# --- Verilog Sources (explicit list, required for BabySoC) ---
set ::env(VERILOG_FILES) "\
$::env(DESIGN_DIR)/src/vsdbabysoc.v \
$::env(DESIGN_DIR)/src/rvmyth.v \
$::env(DESIGN_DIR)/src/rvmyth_gen.v \
$::env(DESIGN_DIR)/src/avsdpll.v \
$::env(DESIGN_DIR)/src/avsddac.v \
$::env(DESIGN_DIR)/src/clk_gate.v \
"

# --- Includes ---
set ::env(VERILOG_INCLUDE_DIRS) "$::env(DESIGN_DIR)/src/include"

# --- Additional Macro Files ---
set ::env(EXTRA_LIBS)  [glob $::env(DESIGN_DIR)/src/lib/*.lib]
set ::env(EXTRA_LEFS)  [glob $::env(DESIGN_DIR)/src/lef/*.lef]
set ::env(EXTRA_GDS_FILES) [glob $::env(DESIGN_DIR)/src/gds/*.gds]

# --- Timing ---
set ::env(BASE_SDC_FILE) "$::env(DESIGN_DIR)/src/vsdbabysoc_synthesis.sdc"
set ::env(CLOCK_PORT) "CLK"
set ::env(CLOCK_NET)  "CLK"
set ::env(CLOCK_PERIOD) "20.0"

# --- Floorplan ---
set ::env(FP_PIN_ORDER_CFG) "$::env(DESIGN_DIR)/pin_order.cfg"
set ::env(MACRO_PLACEMENT_CFG) "$::env(DESIGN_DIR)/macro.cfg"

set ::env(FP_SIZING) "absolute"
set ::env(DIE_AREA) "0 0 1500 1500"

set ::env(BOTTOM_MARGIN_MULT) 20
set ::env(TOP_MARGIN_MULT) 20
set ::env(LEFT_MARGIN_MULT) 100
set ::env(RIGHT_MARGIN_MULT) 100

# --- Magic ---
set ::env(MAGIC_ZEROIZE_ORIGIN) 0
set ::env(MAGIC_EXT_USE_GDS) 1

```

### ERROR
```bash
14. Executing ABC pass (technology mapping using ABC).
14.1. Extracting gate netlist of module `\vsdbabysoc' to `<abc-temp-dir>/input.blif'..
yosys-abc: src/map/scl/sclLibUtil.c:77: void abc::Abc_SclHashCells(SC_Lib *): Assertion `*pPlace == -1' failed.
ERROR: ABC failed with status 86Command exited with non-zero status 1
Elapsed time: 0:07.64[h:]min:sec. CPU time: user 4.93 sys 0.22 (67%). Peak memory: 92568KB.
make[1]: *** [Makefile:262: do-yosys] Error 1
make: *** [Makefile:272: results/sky130hd/vsdbabysoc/base/1_2_yosys.v] Error 2
again this error
```
SOLUTION-
Your config file has:
```bash
export ADDITIONAL_LIBS = $(wildcard $(vsdbabysoc_DIR)/lib/*.lib)
```

⚠️ This is wrong
OpenROAD already loads the platform .lib files.
This line may be overwriting them → ABC crashes.So,Comment out that line .

```bash
#export ADDITIONAL_LIBS = $(wildcard $(vsdbabysoc_DIR)/lib/*.lib)
```
### 📌 Before running OpenROAD, verify files exist

Run this in terminal:
```bash
ls designs/sky130hd/vsdbabysoc/src/
```

You MUST see:
```bash
vsdbabysoc.v
rvmyth.v
rvmyth_gen.v
clk_gate.v
avsdpll.v
avsddac.v
```
If anything missing → synthesis will fail.


### 🚀 Now run synthesis
```bash
make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.tcl
```
### ERROR
```bash
[INFO GRT-0018] Total wirelength: 494454 um
[INFO GRT-0014] Routed nets: 6595
[ERROR GRT-0116] Global routing finished with congestion. Check the congestion regions in the DRC Viewer.
Error: global_route.tcl, 120 GRT-0116
Command exited with non-zero status 1
Elapsed time: 3:59.59[h:]min:sec. CPU time: user 406.93 sys 4.59 (171%). Peak memory: 465120KB.
make[1]: *** [Makefile:547: do-5_1_grt] Error 1
make: *** [Makefile:547: results/sky130hd/vsdbabysoc/base/5_1_grt.odb] Error 2
error after cts
```
 Completed CTS, but global routing failed due to congestion:
```bash
[ERROR GRT-0116] Global routing finished with congestion.
```
You hit a GRT-0116: Global Routing Congestion error after CTS.
This is very common for SoC-scale designs like BabySoC on Sky130HD, especially when the floorplan is too tight or macros are blocking routing channels.


### Why congestion happens after CTS

Common causes:

✔ 1. Die area too small

Your earlier config had:
```bash
set ::env(DIE_AREA) "0 0 1500 1500"
```

For vsdbabysoc, 1500×1500 µm is too small.

✔ 2. Macros are placed too close

(avsdpll, avsddac) → block routing channels.

✔ 3. Utilization too high

Default is ~50%, but with BabySoC it becomes effectively 70–80%.

### ✅ Fix (Guaranteed to remove congestion)

Open your config.tcl and update these:
1. Increase DIE size
2. Lower target density
3. Add more routing tracks (huge improvement)
4. Increase macro spacing

```bash

# ROUTING + PLACEMENT FIXES
set ::env(DIE_AREA) "0 0 2000 2000"
set ::env(PL_TARGET_DENSITY) "0.45"
set ::env(GRT_ALLOW_CONGESTION) 1
set ::env(GRT_ADJUSTMENT) 0.3
set ::env(MACRO_PLACE_CHANNEL) 20
set ::env(MACRO_PLACE_HALO) "20 20"
```
🚀 After modifying config.tcl, run:
```bash
make DESIGN_CONFIG=designs/sky130hd/vsdbabysoc/config.tcl clean_floorplan
make DESIGN_CONFIG=designs/sky130hd/vsdbabysoc/config.tcl -j4

```
Do NOT skip clean_floorplan.

The updated version with die area expansion, lower density, macro padding, and CTS buffer adjustments applied:
```bash

set ::env(DESIGN_NAME) "vsdbabysoc"

# --- Verilog Sources (explicit list, required for BabySoC) ---
set ::env(VERILOG_FILES) "\
$::env(DESIGN_DIR)/src/vsdbabysoc.v \
$::env(DESIGN_DIR)/src/rvmyth.v \
$::env(DESIGN_DIR)/src/rvmyth_gen.v \
$::env(DESIGN_DIR)/src/avsdpll.v \
$::env(DESIGN_DIR)/src/avsddac.v \
$::env(DESIGN_DIR)/src/clk_gate.v \
"

# --- Includes ---
set ::env(VERILOG_INCLUDE_DIRS) "$::env(DESIGN_DIR)/src/include"

# --- Additional Macro Files ---
set ::env(EXTRA_LIBS)  [glob $::env(DESIGN_DIR)/src/lib/*.lib]
set ::env(EXTRA_LEFS)  [glob $::env(DESIGN_DIR)/src/lef/*.lef]
set ::env(EXTRA_GDS_FILES) [glob $::env(DESIGN_DIR)/src/gds/*.gds]

# --- Timing ---
set ::env(BASE_SDC_FILE) "$::env(DESIGN_DIR)/src/vsdbabysoc_synthesis.sdc"
set ::env(CLOCK_PORT) "CLK"
set ::env(CLOCK_NET)  "CLK"
set ::env(CLOCK_PERIOD) "20.0"

# --- Floorplan ---
set ::env(FP_PIN_ORDER_CFG) "$::env/DESIGN_DIR/pin_order.cfg"
set ::env(MACRO_PLACEMENT_CFG) "$::env/DESIGN_DIR/macro.cfg"

set ::env(FP_SIZING) "absolute"

# --- ✅ Updated DIE AREA for congestion relief ---
set ::env(DIE_AREA) "0 0 2200 2200"

# --- Margins ---
set ::env(BOTTOM_MARGIN_MULT) 20
set ::env(TOP_MARGIN_MULT) 20
set ::env(LEFT_MARGIN_MULT) 100
set ::env(RIGHT_MARGIN_MULT) 100

# --- Density / Utilization (Sky130 prefers <0.5) ---
set ::env(CORE_UTILIZATION) "28"
set ::env(PL_TARGET_DENSITY) "0.45"

# --- Macro placement padding to open routing channels ---
set ::env(MACRO_PLACE_HALO) "20 20"
set ::env(MACRO_PLACE_CHANNEL) "30 30"

# --- Allow more global routing iterations to tolerate congestion ---
set ::env(GRT_ALLOW_CONGESTION) 1
set ::env(GRT_MAX_DENSITY) 0.95
set ::env(GRT_ADJUSTMENT) 0.15

# --- CTS buffer tuning (less aggressive) ---
set ::env(CTS_ROOT_BUFFER) "sky130_fd_sc_hd__clkbuf_2"

# --- Magic ---
set ::env(MAGIC_ZEROIZE_ORIGIN) 0
set ::env(MAGIC_EXT_USE_GDS) 1
```

so on running 
```bash
make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.tcl \PLATFORM=sky130hd \DESIGN_NAME=vsdbabysoc \-j2
```
### ERROR

```bash
designs/sky130hd/vsdbabysoc/config.tcl:4: *** multiple target patterns. Stop.
```

SOLUTION
```bash
make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.tcl \
     PLATFORM=sky130hd \
     DESIGN_NAME=vsdbabysoc \
     -j2
```
### Practical ways to fix GRT-0116

1.Increase die area further

-If feasible, increase it gradually (e.g., 2200–2500) and rerun placement & GRT.

2.Adjust GRT congestion thresholds
-In global_route.tcl or config.tcl, look for options like:
```bash
set_max_congestion 0.8
```
-Increasing the allowed congestion may let routing complete.

3.Enable layer assignment / route layer optimization

-Check your OpenROAD GRT settings for vertical_layer_bias or route_layers and increase number of available routing layers if possible.

4.Run incremental placement optimization
-Sometimes re-running cts → placement → legalization with slightly looser spacing helps.

5.Check macros / IO placement

-Congestion often happens near the IO pads or large macros.
-Move large macros or spread them out.

Quick checks you can do
```bash
openroad -gui
read_def <your_def_file>
view_congestion
```
But the files exist in .odb not .db as follows
```bash
/workspaces/vsd-pd/OpenROAD-flow-scripts/flow/results/s
ky130hd/vsdbabysoc/base$ ls
1_1_yosys_canonicalize.rtlil  2_4_floorplan_pdn.odb     3_place.odb
1_2_yosys.v                   2_floorplan.odb           3_place.sdc
1_synth.sdc                   2_floorplan.sdc           4_1_cts.odb
1_synth.v                     3_1_place_gp_skip_io.odb  4_cts.odb
2_1_floorplan.odb             3_2_place_iop.odb         4_cts.sdc
2_1_floorplan.sdc             3_2_place_iop.tcl         5_1_grt-failed.odb
2_2_floorplan_macro.odb       3_3_place_gp.odb          clock_period.txt
2_2_floorplan_macro.tcl       3_4_place_resized.odb     mem.json
2_3_floorplan_tapcell.odb     3_5_place_dp.odb
```
1. .odb → OpenROAD Design Binary database (ODB), used internally by OpenROAD for placement, CTS, and routing.

2. .def → optional export from ODB; OpenROAD can read/write DEF, but the flow doesn’t always export it by default.

So the absence of .def is normal if the flow only produces ODB files.

### Solution
```bash

openroad -gui            -> in the terminal with correct path in novnc desktop
read_db 2_1_floorplan.odb    -> in the tcl command inside gui

```
















