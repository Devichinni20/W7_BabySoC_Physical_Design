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
 <img width="572" height="570" alt="image" src="https://github.com/user-attachments/assets/67978026-7374-4f7f-b66d-3815e77f3868" />


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

3️⃣ Name the file

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
<img width="1507" height="726" alt="Screenshot (459)" src="https://github.com/user-attachments/assets/e970ce82-2286-4241-a6f5-f1a9efdbc26a" />

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
->Floorplanning
->Placement
->Clock tree synthesis
->Routing
->GDSII generation

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

<img width="1465" height="398" alt="Screenshot (453)" src="https://github.com/user-attachments/assets/b4ee3841-90ee-4c37-87b7-49f8b7944a85" />


### ERROR
```bash
 make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.mk
designs/sky130hd/vsdbabysoc/config.mk:11: *** missing separator (did you mean TAB instead of 8 spaces?).  Stop.
```
<img width="1519" height="672" alt="Screenshot (455)" src="https://github.com/user-attachments/assets/7ad8a51b-9977-4b1e-a9d1-d5bea3597ac8" />

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


<img width="1538" height="808" alt="Screenshot (463)" src="https://github.com/user-attachments/assets/0bcdbd72-858b-4fe5-a042-cf32083b3ae1" />



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
or
make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.tcl
```

### SYNTHESIS

<img width="1526" height="808" alt="Screenshot (461)" src="https://github.com/user-attachments/assets/56477bf9-fca1-4072-b1ab-37fc3c1327dc" />
<img width="1529" height="815" alt="Screenshot (462)" src="https://github.com/user-attachments/assets/ba4609a8-2f8b-4d3f-a3ef-59e8ecb47eac" />

### FLOORPLAN

<img width="1368" height="806" alt="Screenshot (464)" src="https://github.com/user-attachments/assets/6f4e0143-d4a2-4285-a3cf-9b7111ef7ad5" />
<img width="1432" height="819" alt="Screenshot (465)" src="https://github.com/user-attachments/assets/07e4de19-be84-47f5-a767-bf4e3048c45c" />
<img width="1420" height="800" alt="Screenshot (466)" src="https://github.com/user-attachments/assets/eb09327c-cccb-46fc-8d73-83d94304c106" />

### GLOBAL PLACE_REPORT_DESIGN_AREA

<img width="1427" height="809" alt="Screenshot (467)" src="https://github.com/user-attachments/assets/9b17e642-95e7-47db-b938-a58550d26f86" />

### PLACEMENT ANALYSIS

<img width="1445" height="809" alt="Screenshot (468)" src="https://github.com/user-attachments/assets/e9fd7254-7e2a-4f00-8a75-284ffd01048b" />

### CTS FINAL REPORT

```bash

vscode@codespaces-f73089:/workspaces/vsd-pd$ cd /workspaces/vsd-pd/OpenROAD-flow-scripts/flow
vscode@codespaces-f73089:/workspaces/vsd-pd/OpenROAD-flow-scripts/flow$ make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.mk 
/workspaces/vsd-pd/OpenROAD-flow-scripts/flow/scripts/flow.sh 5_1_grt global_route
Running global_route.tcl, stage 5_1_grt
read_liberty /workspaces/vsd-pd/OpenROAD-flow-scripts/flow/platforms/sky130hd/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
read_db ./results/sky130hd/vsdbabysoc/base/4_cts.odb
[INFO DRT-0149] Reading tech and libs.
[WARNING DRT-0349] LEF58_ENCLOSURE with no CUTCLASS is not supported. Skipping for layer mcon
[WARNING DRT-0349] LEF58_ENCLOSURE with no CUTCLASS is not supported. Skipping for layer mcon
[WARNING DRT-0349] LEF58_ENCLOSURE with no CUTCLASS is not supported. Skipping for layer via
[WARNING DRT-0349] LEF58_ENCLOSURE with no CUTCLASS is not supported. Skipping for layer via
[WARNING DRT-0349] LEF58_ENCLOSURE with no CUTCLASS is not supported. Skipping for layer via2
[WARNING DRT-0349] LEF58_ENCLOSURE with no CUTCLASS is not supported. Skipping for layer via2
[WARNING DRT-0349] LEF58_ENCLOSURE with no CUTCLASS is not supported. Skipping for layer via3
[WARNING DRT-0349] LEF58_ENCLOSURE with no CUTCLASS is not supported. Skipping for layer via3
[WARNING DRT-0349] LEF58_ENCLOSURE with no CUTCLASS is not supported. Skipping for layer via4
[WARNING DRT-0349] LEF58_ENCLOSURE with no CUTCLASS is not supported. Skipping for layer via4

Units:                1000
Number of layers:     13
Number of macros:     443
Number of vias:       30
Number of viarulegen: 25

[INFO DRT-0150] Reading design.
[WARNING DRT-0120] Large net net571 has 148 pins which may impact routing performance. Consider optimization.

Design:                   vsdbabysoc
Die area:                 ( 0 0 ) ( 1600000 1600000 )
Number of track patterns: 12
Number of DEF vias:       0
Number of components:     30378
Number of terminals:      9
Number of snets:          2
Number of nets:           6629

[INFO DRT-0167] List of default vias:
  Layer via
    default via: M1M2_PR
  Layer via2
    default via: M2M3_PR
  Layer via3
    default via: M3M4_PR
  Layer via4
    default via: M4M5_PR
[INFO DRT-0162] Library cell analysis.
[INFO DRT-0163] Instance analysis.
[INFO DRT-0164] Number of unique instances = 217.
[INFO DRT-0168] Init region query.
[INFO DRT-0024]   Complete FR_MASTERSLICE.
[INFO DRT-0024]   Complete Fr_VIA.
[INFO DRT-0024]   Complete li1.
[INFO DRT-0024]   Complete mcon.
[INFO DRT-0024]   Complete met1.
[INFO DRT-0024]   Complete via.
[INFO DRT-0024]   Complete met2.
[INFO DRT-0024]   Complete via2.
[INFO DRT-0024]   Complete met3.
[INFO DRT-0024]   Complete via3.
[INFO DRT-0024]   Complete met4.
[INFO DRT-0024]   Complete via4.
[INFO DRT-0024]   Complete met5.
[INFO DRT-0033] FR_MASTERSLICE shape region query size = 0.
[INFO DRT-0033] FR_VIA shape region query size = 0.
[INFO DRT-0033] li1 shape region query size = 280837.
[INFO DRT-0033] mcon shape region query size = 148352.
[INFO DRT-0033] met1 shape region query size = 95925.
[INFO DRT-0033] via shape region query size = 119585.
[INFO DRT-0033] met2 shape region query size = 71828.
[INFO DRT-0033] via2 shape region query size = 95650.
[INFO DRT-0033] met3 shape region query size = 71766.
[INFO DRT-0033] via3 shape region query size = 95644.
[INFO DRT-0033] met4 shape region query size = 29571.
[INFO DRT-0033] via4 shape region query size = 5461.
[INFO DRT-0033] met5 shape region query size = 5691.
[INFO DRT-0165] Start pin access.
[INFO DRT-0076]   Complete 1000 pins.
[WARNING DRT-6000] Macro pin has more than 1 polygon
[WARNING DRT-6000] Macro pin has more than 1 polygon
[WARNING DRT-6000] Macro pin has more than 1 polygon
[WARNING DRT-6000] Macro pin has more than 1 polygon
[WARNING DRT-6000] Macro pin has more than 1 polygon
[WARNING DRT-6000] Macro pin has more than 1 polygon
[WARNING DRT-6000] Macro pin has more than 1 polygon
[WARNING DRT-6000] Macro pin has more than 1 polygon
[WARNING DRT-6000] Macro pin has more than 1 polygon
.
.
.
[WARNING DRT-6000] Macro pin has more than 1 polygon
[WARNING DRT-6000] Macro pin has more than 1 polygon
[WARNING DRT-6000] Macro pin has more than 1 polygon
[WARNING DRT-6000] Macro pin has more than 1
[INFO DRT-0078]   Complete 1784 pins.
[INFO DRT-0079]   Complete 100 unique inst patterns.
[INFO DRT-0079]   Complete 200 unique inst patterns.
[INFO DRT-0081]   Complete 215 unique inst patterns.
[INFO DRT-0084]   Complete 3686 groups.
#scanned instances     = 30378
#unique  instances     = 217
#stdCellGenAp          = 6979
#stdCellValidPlanarAp  = 73
#stdCellValidViaAp     = 5131
#stdCellPinNoAp        = 6
#stdCellPinCnt         = 23186
#instTermValidViaApCnt = 0
#macroGenAp            = 1679
#macroValidPlanarAp    = 1370
#macroValidViaAp       = 81
#macroNoAp             = 0
[INFO DRT-0166] Complete pin access.
[INFO DRT-0267] cpu time = 00:06:36, elapsed time = 00:03:48, memory = 234.11 (MB), peak = 236.85 (MB)
global_route -congestion_report_file ./reports/sky130hd/vsdbabysoc/base/congestion.rpt -congestion_iterations 30 -congestion_report_iter_step 5 -verbose
[INFO GRT-0020] Min routing layer: met1
[INFO GRT-0021] Max routing layer: met5
[INFO GRT-0022] Global adjustment: 0%
[INFO GRT-0023] Grid origin: (0, 0)
[INFO GRT-0088] Layer li1     Track-Pitch = 0.4600  line-2-Via Pitch: 0.3400
[INFO GRT-0088] Layer met1    Track-Pitch = 0.3400  line-2-Via Pitch: 0.3400
[INFO GRT-0088] Layer met2    Track-Pitch = 0.4600  line-2-Via Pitch: 0.3500
[INFO GRT-0088] Layer met3    Track-Pitch = 0.6800  line-2-Via Pitch: 0.6150
[INFO GRT-0088] Layer met4    Track-Pitch = 0.9200  line-2-Via Pitch: 1.0400
[INFO GRT-0088] Layer met5    Track-Pitch = 3.4000  line-2-Via Pitch: 3.1100
[INFO GRT-0003] Macros: 2
[INFO GRT-0004] Blockages: 17305
[INFO GRT-0019] Found 94 clock nets.
[INFO GRT-0001] Minimum degree: 2
[INFO GRT-0002] Maximum degree: 148

[INFO GRT-0053] Routing resources analysis:
          Routing      Original      Derated      Resource
Layer     Direction    Resources     Resources    Reduction (%)
---------------------------------------------------------------
li1        Vertical            0            10          0.00%
met1       Horizontal    1071378        459545          57.11%
met2       Vertical       803418        399727          50.25%
met3       Horizontal     535689        297307          44.50%
met4       Vertical       322014        144702          55.06%
met5       Horizontal     106953         41589          61.11%
---------------------------------------------------------------

[INFO GRT-0101] Running extra iterations to remove overflow.
[INFO GRT-0197] Via related to pin nodes: 44078
[INFO GRT-0198] Via related Steiner nodes: 1182
[INFO GRT-0199] Via filling finished.
[INFO GRT-0111] Final number of vias: 58489
[INFO GRT-0112] Final usage 3D: 228146

[INFO GRT-0096] Final congestion report:
Layer         Resource        Demand        Usage (%)    Max H / Max V / Total Overflow
---------------------------------------------------------------------------------------
li1                 10             0            0.00%             0 /  0 /  0
met1            459545         23092            5.02%             1 /  0 /  5
met2            399727         15562            3.89%             0 /  1 /  7
met3            297307         10939            3.68%             1 /  0 / 11
met4            144702          2264            1.56%             0 /  1 /  4
met5             41589           822            1.98%             1 /  0 /  5
---------------------------------------------------------------------------------------
Total          1342880         52679            3.92%             3 /  2 / 32

[INFO GRT-0018] Total wirelength: 494454 um
[INFO GRT-0014] Routed nets: 6595
[ERROR GRT-0116] Global routing finished with congestion. Check the congestion regions in the DRC Viewer.
Error: global_route.tcl, 120 GRT-0116
Command exited with non-zero status 1
Elapsed time: 4:00.74[h:]min:sec. CPU time: user 407.00 sys 3.59 (170%). Peak memory: 464952KB.
make[1]: *** [Makefile:547: do-5_1_grt] Error 1
make: *** [Makefile:547: results/sky130hd/vsdbabysoc/base/5_1_grt.odb] Error 2

```

<img width="1431" height="793" alt="Screenshot (469)" src="https://github.com/user-attachments/assets/8a6e7be6-896c-4955-986a-0eeb205a19ad" />

<img width="1452" height="807" alt="Screenshot (470)" src="https://github.com/user-attachments/assets/6686ede5-50ee-401a-acc1-b94072a20d33" />
<img width="1431" height="821" alt="Screenshot (471)" src="https://github.com/user-attachments/assets/173c729c-2996-48c9-beeb-ec54d87fac96" />

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

<img width="1461" height="815" alt="Screenshot (474)" src="https://github.com/user-attachments/assets/b21595df-5467-4c64-a1ae-0ceca44ac013" />
<img width="1507" height="802" alt="Screenshot (475)" src="https://github.com/user-attachments/assets/cd6637dd-143b-46e7-8636-1cafc89b0f5d" />

<img width="1395" height="811" alt="Screenshot (476)" src="https://github.com/user-attachments/assets/ffe7cdd3-7bf8-44e4-b739-e2d727cc1f50" />



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

<img width="1421" height="801" alt="Screenshot (478)" src="https://github.com/user-attachments/assets/ad99d079-ee69-4376-a46f-934d27de1966" />

<img width="1593" height="920" alt="Screenshot (480)" src="https://github.com/user-attachments/assets/d2e32d31-d8ce-4a97-8b16-a864e36632d2" />
<img width="1595" height="927" alt="Screenshot (481)" src="https://github.com/user-attachments/assets/74ee46d5-5ed8-4988-9356-09f29e304046" />
<img width="1588" height="931" alt="Screenshot (484)" src="https://github.com/user-attachments/assets/f24002f2-0e28-4914-a0c9-98c1750d620f" />

### ERRORS
<img width="1603" height="925" alt="Screenshot (490)" src="https://github.com/user-attachments/assets/45cb0585-a2ee-425a-b00d-abb3cb0f59fa" />

<img width="1601" height="921" alt="Screenshot (491)" src="https://github.com/user-attachments/assets/5ace33be-0bd9-4042-8e95-83eca48e6ee8" />




### Solution
```bash

openroad -gui            -> in the terminal with correct path in novnc desktop
read_db 2_1_floorplan.odb    -> in the tcl command inside gui

```

<img width="1595" height="918" alt="Screenshot (492)" src="https://github.com/user-attachments/assets/4bba1809-59b7-4b09-9396-9644e7481c33" />

<img width="1599" height="920" alt="Screenshot (493)" src="https://github.com/user-attachments/assets/19820f3d-1ebf-466c-8090-f14127483479" />

<img width="1595" height="903" alt="Screenshot (494)" src="https://github.com/user-attachments/assets/8b3bc7e0-d235-4a2f-bfb0-b603015098bb" />










