# W7_BabySoC_Physical_Design

<details>
  <summary>
 THEORY
  </summary>


#### Path to Zetta-Scale Computing

**Introduction:**

- **Bombe:** The Bombe was an electro-mechanical machine designed during World War II to decrypt German Enigma-encrypted messages. It was refined and built by Alan Turing and Gordon Welchman at Bletchley Park, UK. The Bombe systematically tested possible rotor settings of the Enigma machine by exploiting known plaintext patterns. Its logical operations helped narrow down the vast number of possible keys, significantly accelerating the decryption process. The Bombe played a critical role in the Allied war effort.

- **ENIAC (Electronic Numerical Integrator and Computer):** It was developed during World War II by John Presper Eckert and John Mauchly at the University of Pennsylvania, was the first general-purpose, fully electronic digital computer. Completed in 1945, it was designed to compute artillery firing tables for the U.S. Army. ENIAC used vacuum tubes instead of mechanical or electromechanical components. However, it lacked a stored-program capability, requiring manual reconfiguration for each new task. ENIAC demonstrated the immense potential of electronic computing for large-scale numerical problems.

- **EDVAC (Electronic Discrete Variable Automatic Computer):** EDVAC, also developed by Eckert and Mauchly with conceptual input from John von Neumann, was one of the first computers to implement the stored-program concept. Completed in 1949, EDVAC represented a significant improvement over ENIAC by using binary representation instead of decimal and storing both data and instructions in memory. This innovation simplified programming and laid the groundwork for the modern von Neumann architecture.

**50 Years of Microprocessor Trend Data:**
<img width="864" height="409" alt="image" src="https://github.com/user-attachments/assets/87b43396-2a2c-48bf-8153-5c6cab57b563" />

**The Key metrics are:**

- **Transistors (Orange Triangles):** The number of transistors on a microprocessor chip (in thousands) has increased exponentially, following Moore's Law, which predicts a doubling approximately every two years. This growth enabled more complex and capable processors, reaching the range of billions of transistors by the 2020s.
- **Single-Thread Performance (Blue Circles):** It is measured using SpecINT. It indicates the computational ability of a single processor core. Performance grew steadily due to improvements in architecture, instruction-level parallelism, and clock speeds, but the growth rate slowed post-2005 due to physical limitations like power and heat.
- **Frequency (Green Diamonds):** Processor clock speed (in MHz) rose steadily until the early 2000s but then stagnated as increasing clock speeds became inefficient due to heat dissipation issues.
- **Typical Power (Red Triangles):** Power consumption increased with transistor density and frequency, becoming a critical design challenge around the mid-2000s.
- **Number of Logical Cores (Black Dots):** The transition to multi-core processors gained momentum in the mid-2000s as a response to the stagnation in single-thread performance. By increasing the number of cores, processors enabled more efficient parallel processing, leading to significant improvements in overall performance

**Key Milestones**

- **iPhone Release (~2007):** Signals the emergence of mobile computing, where power efficiency became as crucial as performance. This catalyzed innovations in low-power processor designs.
- **Datacenter-Scale Computing (Post-2010):** Marks the rise of cloud computing and large-scale data centers, where energy efficiency, scalability, and parallelism became central concerns.

**Path to zetta-scale computing**
<img width="1019" height="514" alt="image" src="https://github.com/user-attachments/assets/54bb513c-a3ef-49ff-843c-b07c2d41fc63" />

The path to zetta-scale computing, tracing the evolution of computing performance (measured in FLOPS—floating-point operations per second) from the gigascale era in 1984 to the projected zettascale by 2035.

**Key Performance Levels**

- **Gigascale (10⁹ FLOPS):** The starting point in 1984, marking the capability of early supercomputers.
- **Terascale (10¹² FLOPS):** Achieved around 1997, a significant milestone where systems like Jaguar (Cray XT5) delivered teraflop performance with power consumption of 7 MW.
- **Petascale (10¹⁵ FLOPS):** Achieved in 2008 with systems like Titan (Cray XK6) at 27 petaflops, consuming 9 MW. This milestone represents the era of petascale high-performance computing (HPC).
- **Exascale (10¹⁸ FLOPS):** Reached by systems like Frontier (Cray Shasta) in 2021, delivering 1.5 exaflops using 4 AMD GPUs and 1 AMD CPU, consuming 29 MW of power. Exascale computing enables highly detailed simulations and large-scale AI workloads.
- **Zettascale (10²¹ FLOPS):** Projected to be achieved by around 2035. At this scale, systems will handle unprecedented computational workloads, such as advanced climate modeling, AI, and large-scale simulations. Power consumption is estimated to range between 50-100 MW for a single zettascale machine.
**CMOS Evolution and Next-Gen Candidates**

<img width="1013" height="474" alt="image" src="https://github.com/user-attachments/assets/9f794d76-f828-4cf2-b634-58c7de7dfd87" />
This diagram illustrates the evolving landscape of CMOS (Complementary Metal-Oxide-Semiconductor) technology and highlights emerging materials, structures, and processes being explored for next-generation semiconductor devices. These innovations aim to address the challenges of scaling CMOS technology down to the 1nm node and beyond.


- **Channel Material**
  - **Current Trends**: 
    - Silicon (Si) is the primary material used for the channel in traditional CMOS transistors, with **strained SiGe** (Silicon-Germanium) being used in some high-performance applications to enhance carrier mobility.
  
  - **Future Materials**: 
    - **2D materials** such as MoS₂ (Molybdenum Disulfide) are being explored due to their potential for better electrical characteristics at smaller scales.
    - **Germanium (Ge)** is gaining interest as it offers higher electron mobility, which could significantly boost transistor performance at small nodes.

- **Patterning**
  - **Current Techniques**: 
    - **Deep Ultraviolet (DUV)** lithography is the most commonly used technique for defining transistor features, with **ArF (Argon Fluoride)** and **KrF (Krypton Fluoride)** lasers operating at different wavelengths.
  
  - **Next-Gen**: 
    - **Extreme Ultraviolet (EUV)** lithography is expected to be a key technology for sub-7nm nodes. **High-NA (Numerical Aperture) EUV** will further improve the resolution for even smaller transistor nodes, pushing the boundaries of Moore's Law.

- **Gate Stack Material**
  - **Current Materials**: 
    - **High-K metal gates (HKMG)** are used in the gate stack of modern FETs to reduce gate leakage current and improve switching performance.
  
  - **Next-Gen Candidates**:
    - **NC-FET (Negative Capacitance FET)**: This is a promising transistor design that leverages ferroelectric materials to reduce power consumption by enabling lower voltage operation.
    - **TFET (Tunnel FET)**: TFETs use quantum tunneling to switch on and off, offering a significant reduction in power consumption compared to conventional FETs, especially for low-power applications.

- **Interconnection Material**
  - **Current Materials**: 
    - **Copper (Cu)** is the primary material used for interconnects due to its low resistivity, which helps in minimizing power loss and delays in transistor connections.
  
  - **Next-Gen Materials**:
    - **Ruthenium (Ru)** and **Compound metals** are being investigated for their potential to reduce resistance and improve performance in ultra-small transistors.
    - **Topological semi-metals** may offer unique properties, such as lower resistivity and increased performance at the atomic scale.


- **Device Structure**
  - **Current Architectures**: 
    - **FinFET** and **planar** transistors are used to maintain performance at smaller nodes. FinFETs, in particular, help improve control over short-channel effects by using a 3D structure.
  
  - **Next-Gen Architectures**:
    - **3DS-FET (3D Stacked FET)**: These are three-dimensional transistors where multiple layers of devices are stacked vertically, reducing footprint and improving performance.
    - **MBC-FET (Multi-Bridge Channel FET)**: This structure aims to enhance drive current by creating multiple channels within the same device.
    - **VFET (Vertical FET)**: VFETs utilize vertical channels to improve density and reduce power consumption.

- **Design Co-Optimization**
  - **DTCO (Design-Technology Co-Optimization)**: 
    - DTCO focuses on integrating new design techniques with advanced process technologies to maximize chip performance, often involving **backside interconnects (BSI)**, where interconnections are made at the back of the wafer for improved signal integrity and reduced latency.
  
  - **STCO (System-Technology Co-Optimization)**: 
    - This approach involves optimizing both the system architecture and the underlying technology. One example is the use of **chiplets**, which allow for modular, customized designs by integrating multiple smaller chips into one package, offering flexibility and reducing the complexity of scaling single-chip designs.

#### FinFETs
<img width="1002" height="536" alt="image" src="https://github.com/user-attachments/assets/5070e7f4-a1a2-429c-853c-39296712b2ac" />

This diagram illustrates the evolution of transistor technology from planar to more advanced architectures like FinFET and Gate-All-Around (GAA):

1. **Planar Transistor (Traditional)**:
   - Early transistor design with a flat channel and gate structure.
   - The gate controls the channel from one side only, leading to limited performance as scaling continues.

2. **FinFET (2011)**:
   - The channel is shaped like a vertical fin, allowing the gate to wrap around three sides of the channel.
   - Provides better control over the channel, reducing leakage and improving performance at smaller sizes.

3. **Gate-All-Around (GAA) Transistor (2025?)**:
   - The gate completely surrounds the channel, typically implemented using stacked nanosheets or nanowires.
   - Offers even better control over the channel compared to FinFET, allowing higher performance and efficiency with continued scaling.

Each step improves drive current capability and enhances control over the transistor's on/off states, critical for power efficiency and miniaturization in modern electronics.

**Why FinFETs and Gate-All-Around Transistors?**

<img width="1019" height="554" alt="image" src="https://github.com/user-attachments/assets/058430c7-c598-4d37-abd1-dbf1ee5d7b6f" />

This diagram explains the advantages of FinFETs and Gate-All-Around (GAA) transistors compared to traditional planar structures:

 1. **Planar Transistors:**
   - **Challenges:**
     - Sub-channel leakage occurs where current leaks underneath the gate.
     - Results in reduced efficiency.
     - Increases power consumption.

2. **FinFET Transistors:**
   - The gate wraps around the channel (fin) on three sides, providing better control over the channel.
   - **Benefits:**
     - Reduces sub-threshold leakage.
     - Enhances drive current (\(I_{ON}\)).
     - Allows a smaller transistor area while maintaining high performance.

3. **Gate-All-Around (GAA) Transistors:**
   - The gate completely surrounds the channel, offering superior electrostatic control.
   - **Advantages:**
     - Improves short-channel performance by reducing drain capacitance and enhancing gate capacitance.
     - Improves scaling efficiency as indicated by the formula \(S \propto (1 + C_d / C_{ox})\).
     - Provides reduced sub-threshold slope and better performance at smaller scales.

4. **Graph Comparison:**
   - Illustrates the performance advantages of FinFETs and GAA over planar transistors.
   - Shows better efficiency and reduced sub-threshold slope as dimensions shrink.
<img width="993" height="499" alt="image" src="https://github.com/user-attachments/assets/c11bb980-1ca1-4bb7-99ef-3bed86f0c926" />

**Reduced Leakage:** Tri-Gate transistors exhibit significantly lower leakage current compared to planar transistors at the same gate voltage. Lower leakage results in both reduced off-current at the same on-current and lower power dissipation.

**Higher Drive Current:** Tri-Gate transistors provide higher drive current compared to planar transistors at the same off-current. This results in improved circuit performance and greater efficiency in modern electronic applications.

#### FEOL Innovations:

FEOL refers to the initial stages of semiconductor manufacturing where the active devices (e.g., transistors) are built on the silicon wafer. It involves creating components such as transistors, capacitors, and isolation structures before metal interconnects are added. FEOL Innovations help drive Moore's Law forward by enabling smaller, more efficient, and more powerful transistors.

**CMOS Technology Inflection Points**

<img width="984" height="552" alt="image" src="https://github.com/user-attachments/assets/fbbea698-acb1-4d8b-92d0-045bd07b9502" />

1. **Dennard Scaling**:
   - States that power density remains constant as transistors shrink.
   - Initially allowed voltage scaling with smaller gate lengths, shown in the bottom-left graph.

2. **Technology Nodes and Innovations**:
   - **~1 µm ("End of Scaling")**: Start of CMOS miniaturization.
   - **180 nm (Voltage Scaling)**: Start of drive voltage reduction.
   - **130 nm (Cu BEOL)**: Introduction of copper interconnects for better conductivity.
   - **90 nm (Uniaxial Strained Si NMOS)**: Strained silicon enhances electron mobility.
   - **65 nm (eSiGe CVD ULK)**: Embedded SiGe improves PMOS performance.
   - **45 nm (HK-first MG-last)**: High-k dielectrics and metal gates reduce leakage and improve gate control.
   - **32 nm (HKMG with Raised S/D NMOS)**: Advanced HKMG implementation and raised source/drain regions.

3. **SEM Images**

- **Left Image:** Shows the cross-sectional view of a transistor structure with High-k materials and embedded SiGe (Silicon-Germanium).It has high-k dielectric and metal gates are used to improve performance. SiGe regions enhance PMOS performance by applying strain to the silicon channel.

- **Right Image:** Demonstrates the raised source/drain (S/D) regions and gate channel in PMOS transistors at smaller nodes.

4. **Drive Voltage Scaling Graph (Bottom-left):** The graph shows the relationship between gate length (x-axis, logarithmic scale) and drive voltage (y-axis, logarithmic scale). The Ideal scaling behavior indicates that the voltage decreases linearly with shrinking gate length. Red and green markers show practical trends for low-power and high-performance devices, which deviate from ideal scaling due to challenges like leakage currents and increased power density.

<img width="1018" height="560" alt="image" src="https://github.com/user-attachments/assets/cad83545-5810-4675-bb26-9907755592e2" />
**Key Technology Nodes and Innovations**

- **22 nm**:
  - Introduction of **FinFET (Tri-Gate)** transistors, which reduce leakage and improve gate control.
  - Use of **self-aligned contacts (SAC)** and **copper interconnects (Co+Cu BEOL)**.

- **14 nm**:
  - Transition to **unidirectional metal routing** for better density.
  - Implementation of **SADP (Self-Aligned Double Patterning)** and **SDB (Single Diffusion Break)** for precise layout.

- **10 nm**:
  - Adoption of **advanced patterning techniques** such as:
    - **SA-SDB** (Self-Aligned SDB)
    - **LELELE** (Litho-Etch-Litho-Etch-Litho-Etch)
    - **SAQP (Self-Aligned Quadruple Patterning)** for tighter geometries.

- **7 nm**:
  - Introduction of **Extreme Ultraviolet Lithography (EUV)** to simplify the patterning process and reduce overlay errors.

- **5 nm**:
  - Integration of **SiGe (Silicon-Germanium) channels** for PMOS to enhance hole mobility.
  - Use of **EUV SA-LELE** (Self-Aligned Litho-Etch-Litho-Etch).

- **3 nm / 2 nm / 1.4 nm**:
  - Transition to **Gate-All-Around (GAA)** nanosheet transistors for improved electrostatic control.
  - GAA stacks nanosheets or nanowires horizontally to maximize current drive.

- **Sub-1 nm**:
  - Development of **CFET (Complementary FET)**, which vertically stacks NMOS over PMOS to save area.
  - Use of **2D materials**, such as **MoS₂**, for atomic-scale channel thickness in **2D FETs**.
    <img width="1000" height="551" alt="image" src="https://github.com/user-attachments/assets/7f11fc4a-f65c-4209-88d5-7fa37f9ff276" />

The image illustrates how Samsung has scaled down the size of transistors in their successive generations of nodes (10nm, 8nm, 7nm, and 5nm) using a technique called Fin Depopulation. In FinFET transistors, the "fin" is the vertical channel that carries the current. Fin Depopulation involves reducing the number of fins per transistor while keeping the fin width constant. This allows for smaller transistors without compromising performance.

- 10nm (HD): The transistor has a fin height of 420nm and uses 10 fins.
- 8nm (UHD): The fin height is reduced to 378nm, and the number of fins is decreased to 9.
- 7nm (HD): The fin height remains at 27nm, but the number of fins is further reduced to 8.
- 5nm (UHD): The fin height is maintained at 27nm, and the number of fins is decreased to 7.
  <img width="1011" height="544" alt="image" src="https://github.com/user-attachments/assets/efc5ecfc-15e2-41bb-b033-b9c49d1552e5" />

- **Double Diffusion Break (DDB)**: Double Diffusion Break (DDB) involves creating a gap between the source and drain regions of a transistor. This gap is filled with an insulating material, which reduces the effective width of the transistor. By doing so, DDB enables the design of smaller cell sizes, allowing for higher transistor density and improved scalability. A cross-sectional view of a transistor with DDB highlights the insulating gap between the source and drain regions.

- **Single Diffusion Break (SDB)**: Single Diffusion Break (SDB) is similar to DDB but less aggressive. It involves introducing a gap on only one side of the transistor. This approach provides a balanced trade-off between size reduction and maintaining transistor performance. A cross-section of a transistor with SDB highlights the gap on one side, showcasing its simplicity compared to DDB.

- **Contact Over Field Gate (COFG)**: Contact Over Field Gate (COFG) places the gate contact directly over the field oxide region of a transistor. This design reduces lateral spacing between adjacent transistors, enabling smaller cell sizes without significant performance loss. A cross-sectional representation of a transistor with COFG illustrates the positioning of the gate contact over the field oxide.

- **Contact Over Active Gate (COAG)**: Contact Over Active Gate (COAG) is a more aggressive technique than COFG. Here, the gate contact is placed directly over the active gate region of the transistor. This approach enables even smaller cell sizes and higher transistor density, which are critical for advanced semiconductor nodes. A cross-sectional image of a transistor with COAG highlights the gate contact placement over the active gate.

- **Back-Side Power Delivery Network (BS-PDN)**: The Back-Side Power Delivery Network (BS-PDN) is an innovative approach where power supply rails are routed on the backside of the chip. This method reduces the height of the standard cell, creating space for more transistors and improving overall transistor density. Additionally, it enhances power delivery efficiency and reduces resistance, which is crucial for high-performance applications. A schematic of a standard cell with BS-PDN illustrates the positioning of power rails on the backside of the chip.

<img width="1011" height="500" alt="image" src="https://github.com/user-attachments/assets/6bf6e645-c65d-41b5-b204-5c27a7de29f1" />

- **Planar Technology**: In early planar technology nodes (100nm and above), the Vt variability is significantly high, around 130mV. This is due to various factors like process variations, temperature fluctuations, and line-edge roughness.

- **FinFET Technology**: With the advent of FinFET technology (around 22nm), the Vt variability reduces significantly to around 14mV. This improvement is attributed to the better control over the channel length and width in FinFETs compared to planar transistors.

- **NW Technology (Nanowire)**: In the latest nanowire technology (14nm and below), the Vt variability is even lower, around 7mV. This further reduction is due to the precise control over the nanowire dimensions and the reduced impact of process variations.

<img width="975" height="530" alt="image" src="https://github.com/user-attachments/assets/3ae606de-5bb2-4b1f-af28-6258c67fb169" />
**Planar MOSFETs**  
Planar MOSFETs, the traditional architecture, have a simple structure where the gate sits above the channel. In this design, the contact width (\(W_C\)) and gate width (\(W_G\)) are nearly equal, resulting in a ratio of \(W_C / W_G \approx 1\). This leads to a low parasitic resistance, with \(R_{EXT}\) being much smaller than \(R_{ch}\) (\(R_{EXT} / R_{ch} < 1\)). As a result, planar MOSFETs suffer minimal performance degradation due to parasitic resistance.

**FinFETs**  
FinFETs, a 3D transistor design, introduce vertical fins with the gate wrapping around them for improved control. However, the effective contact width decreases relative to the gate width, leading to \(W_C / W_G \approx 1/3\). Consequently, the parasitic resistance becomes comparable to the channel resistance (\(R_{EXT} / R_{ch} \approx 1\)), which begins to impact the performance of the device as it scales.

**Gate-All-Around (GAA) FETs**  
Gate-All-Around (GAA) FETs, which use nanosheets or nanowires, offer even better electrostatic control by fully surrounding the channel with the gate. However, the contact width further decreases compared to the gate width, resulting in \(W_C / W_G \approx 1/6\). This causes a significant increase in parasitic resistance, with \(R_{EXT}\) being approximately three times the channel resistance (\(R_{EXT} / R_{ch} \approx 3\)). While GAA FETs improve transistor density, the higher parasitic resistance becomes a challenge for maintaining performance.

**Complementary FETs (CFETs)**  
Complementary FETs (CFETs) take transistor stacking to the next level by vertically integrating NMOS and PMOS transistors. This approach maximizes space efficiency in advanced nodes but inherits the high parasitic resistance of GAA FETs. With \(W_C / W_G\) remaining small, the \(R_{EXT} / R_{ch}\) ratio is around 3, posing similar challenges to those faced by GAA FETs.

**Explanation of Parasitic Resistance**
<img width="993" height="535" alt="image" src="https://github.com/user-attachments/assets/3f8c8104-3943-44a6-88db-0193d18c9526" />
The image highlights the breakdown of parasitic resistance (\(R_{EXT}\)) and approaches for reducing it in transistors. Here is a detailed explanation:

1. **Components of Parasitic Resistance (\(R_{EXT}\))**
The leftmost diagram illustrates the various contributors to \(R_{EXT}\) in a transistor:
- **\(R_{CA-BEOL}\)**: Resistance from the contact in the Back-End-Of-Line (BEOL).
- **\(R_{CA}\)**: Resistance at the contact area.
- **\(R_{CA-TS}\)**: Resistance at the contact to the transition structure.
- **\(R_{TS}\)**: Resistance in the transition structure.
- **\(R_{MOL}\)**: Middle-Of-Line resistance (includes lateral and vertical contributions).
- **\(R_C\)**: Contact resistance at the metal-semiconductor interface.
- **\(R_{EPI}\)**: Epitaxial layer resistance (contributes to current spreading).
- **\(R_{FEOL}\)**: Front-End-Of-Line resistance from the source/drain extensions.

2. **Initial vs. Improved \(R_{EXT}\) Breakdown**
The two pie charts in the center show the contributions of different resistance components for NFETs and PFETs before and after improvements:
- **NFET**:
  - **Initial**: Majority of \(R_{EXT}\) comes from \(R_C\) (63%) and \(R_{CA-BEOL}\) (31%).
  - **Improved**: Significant reduction in \(R_C\) (48%) and \(R_{CA-BEOL}\) (12%).
- **PFET**:
  - **Initial**: \(R_{FEOL}\) (50%) and \(R_C\) (45%) dominate.
  - **Improved**: Major reduction in \(R_{FEOL}\) (78%) and \(R_C\) (16%).

3. **Improving Ohmic/Tunneling Contacts**
The right section discusses methods to improve the metal-semiconductor interface:
- **Key Objectives**:
  - **Low Schottky Barrier Height (SBH)** (\(\phi_b\)): Reduces the energy barrier for carrier injection, enabling better contact conductivity.
  - **High Doping Concentration (\(N_d\))**: Increases carrier density at the interface, reducing contact resistance.
- **Equation for Specific Contact Resistivity (\(\rho_c\))**:
  \[
  \rho_c \propto \exp\left(\frac{2\phi_b}{\hbar} \sqrt{\frac{\epsilon_s m_x}{N_d}}\right)
  \]
  This equation shows how lowering \(\phi_b\) and increasing \(N_d\) can reduce \(\rho_c\).

- **Metal-Semiconductor Energy Diagram**:
  - The energy diagram shows how a reduction in \(\phi_b\) (Schottky Barrier Height) facilitates easier carrier injection from the metal to the semiconductor.
    <img width="1002" height="525" alt="image" src="https://github.com/user-attachments/assets/4275bc32-7d64-4bff-b2c5-82525ae230aa" />

The bar chart on the left shows how the composition of \(C_{eff}\) evolves from 22nm to 7nm technology nodes:

- At **22nm**, the dominant contributor to \(C_{eff}\) is \(C_{fr}\) (56%), while parasitic capacitances \(C_{pc-ca}\) (25%) and \(C_{g}\) (19%) contribute less.
- At **14nm** and **10nm**, parasitic capacitances (\(C_{pc-ca}\) and \(C_{fr}\)) start dominating, with \(C_{fr}\) decreasing to 38% and 25%, respectively, while \(C_{pc-ca}\) increases.
- At **7nm**, \(C_{g}\) becomes the most significant contributor (45%), with \(C_{pc-ca}\) and \(C_{fr}\) still present but reduced. This highlights the increasing impact of parasitic capacitance as node sizes shrink.

Plot Descriptions:

- The first scatter plot shows a reduction in normalized delay for a ring oscillator when using SiBCN spacers instead of SiN spacers, indicating improved performance.
- The second scatter plot demonstrates an 8% reduction in \(C_{eff}\) with SiBCN spacers, which corresponds to the delay improvement observed in the first plot.
- The rightmost figure shows the evolution of spacer materials from SiOCN to SiCO. This material transition aims to significantly reduce the gate-contact capacitance across nodes. At 14nm and beyond, low-\(k\) spacers improve performance by decoupling parasitic effects and maintaining capacitance at manageable levels.
- The bottom middle image shows a cross-sectional TEM view of a transistor with air spacers around the gate: i) Air, with its extremely low dielectric constant (\(k \approx 1\)), significantly reduces parasitic capacitance. The adjacent plot quantifies this improvement, showing a 15% reduction in \(C_{eff}\) when using air spacers compared to solid spacers.

<img width="975" height="531" alt="image" src="https://github.com/user-attachments/assets/58c3a3be-5ea0-4c7a-a9ce-e92518ec3542" />

**Key Properties of 2D Layered Materials (Compared to Silicon):**

- **Uniform Atomic Scale Thickness:** A single layer of MoS₂ is approximately 0.65 nm thick, offering an ideal thickness for scaling compared to silicon. 
- **Higher Effective Mass (\( m^* \)):** MoS₂ has an effective mass of about 0.55 times the mass of a free electron (\( m_0 \)), whereas silicon’s effective mass is around 0.22 \( m_0 \).
- **Bandgap:** Additionally, 2D materials like MoS₂ possess favorable bandgaps for electronic devices, with a monolayer bandgap of ~1.85 eV, which reduces to ~1.5 eV for a bilayer.
<img width="979" height="527" alt="image" src="https://github.com/user-attachments/assets/61972ef3-1be6-4c3f-b559-e4dc0e4824c0" />

1. **Transistor Scaling**:  
   - To achieve smaller gate lengths, devices must address various physical and material constraints to ensure reliable operation.

2. **Challenges for Scaling**:
   - **Direct Source-to-Drain Tunneling**: As the gate length decreases, electrons can tunnel directly from the source to the drain, bypassing the gate control. To mitigate this, materials with a high effective mass (\( m^* \)) are needed.
   - **Surface Roughness and Thickness Variations**: Variability at atomic scales can cause performance issues. Uniform, atomically thin materials are essential for minimizing such variations.
   - **Capacitance Ratios (\( C_D \) and \( C_{ox} \))**: The capacitance of the depletion region (\( C_D \)) must remain low relative to the gate oxide capacitance (\( C_{ox} \)) to improve gate control. Materials with a low in-plane dielectric constant (\( \epsilon \)) are necessary for this.

3. **Diagrams**:  
   - The left shows the transistor structure with key components like the source, drain, gate, oxide, and silicon substrate.
   - The right illustrates two scenarios:  
     a. *Thermionic Emission*: Electrons cross the energy barrier as intended.  
     b. *Direct Tunneling*: At extremely small gate lengths, electrons tunnel directly from source to drain, leading to leakage.

4. **Key Takeaway**:  
   - New channel materials, such as 2D materials, are required to overcome these challenges while maintaining high performance and scalability.
<img width="962" height="541" alt="image" src="https://github.com/user-attachments/assets/4d41988f-d703-4b14-a0c1-19019a332eb4" />

Concept of Direct Source-to-Drain Tunneling: As the gate length (\(L_G\)) in MOSFETs decreases, direct tunneling of electrons from the source to the drain becomes significant, leading to increased leakage currents. This leakage is influenced by material properties, such as the effective mass (\(m^*\)) and the bandgap (\(E_G\)).

A higher \(m^*\) in MoS₂ suppresses tunneling leakage compared to silicon. The graph shows the leakage current (\(I_{SD, \text{leak}}\)) as a function of gate length (\(L_G\)) for various channel thicknesses (\(T_{CH}\)). MoS₂ exhibits lower leakage at smaller gate lengths compared to silicon, achieving up to 100x reduction in leakage due to its higher \(m^*\), larger \(E_G\), and lower dielectric constant (\(\epsilon\)).

The superior performance of MoS₂ in minimizing leakage currents results in significant energy savings, making it a promising material for future transistor scaling.
<img width="975" height="541" alt="image" src="https://github.com/user-attachments/assets/68267a8b-6bfb-4c97-a018-f14483189df5" />
The MoS₂ transistor with a 1 nm gate length represents a breakthrough in miniaturization, featuring a thin MoS₂ channel for its excellent electronic properties. A single-walled carbon nanotube (SWCNT) serves as the ultra-small gate electrode, while Zirconium Dioxide (ZrO₂) acts as a high-k dielectric, reducing leakage and ensuring precise control. Built on a SiO₂ substrate with an n⁺ silicon back gate, the transistor uses the CNT gate to deplete a small region of the MoS₂ channel, enabling efficient modulation. This innovative design showcases the potential of 2D materials and nanoscale gates in advancing transistor technology.
<img width="982" height="530" alt="image" src="https://github.com/user-attachments/assets/fa6e8b8f-3a46-480d-bf08-f7a6abb7047e" />

The slide illustrates the structure and fabrication of an All-2D MOSFET (Metal-Oxide-Semiconductor Field-Effect Transistor), where all key components, including the channel, gate, and contacts, are made using two-dimensional materials. This device leverages the exceptional properties of 2D materials to improve performance and scalability. Below is a breakdown of the key components and the fabrication process:

**Graphene Contacts (S, D, G):** Graphene is used as the source, drain, and gate electrodes. Its high conductivity and 2D nature make it ideal for ensuring low-resistance electrical contacts.
MoS₂ Channel:

**Molybdenum Disulfide (MoS₂)** serves as the semiconductor channel. MoS₂ is widely used in 2D MOSFETs due to its excellent on/off current ratio and atomic-scale thickness.
h-BN Dielectric:

**Hexagonal Boron Nitride (h-BN)** acts as the insulating dielectric layer. It is a 2D material with excellent insulating properties and high thermal stability, making it suitable for separating the graphene gate from the MoS₂ channel.
Si/SiO₂ Substrate:

The device is fabricated on a silicon dioxide (SiO₂) layer on top of a silicon substrate, which provides mechanical support and a global back gate.
Fabrication Process:

- A layer of graphene is deposited on the SiO₂ substrate, which will later serve as the gate electrode.
- Graphene is patterned to define the source and drain regions, leaving gaps for the channel.
- A monolayer of MoS₂ is transferred onto the patterned graphene, forming the channel region.
- An h-BN layer is added on top of the MoS₂ as the gate dielectric.
- A top layer of graphene is deposited and aligned as the gate electrode.
- The completed device is contacted using metallic electrodes (Ni/Au) for testing.
  <img width="936" height="551" alt="image" src="https://github.com/user-attachments/assets/a11b061c-1dd8-4633-b537-9d844bfc146c" />

The All-2D MOSFET exhibits excellent electrical performance:

- **Transfer Characteristics (I\(_D\) vs V\(_G\))**: Achieves a high on/off current ratio (>10⁵), demonstrating strong gate control for effective switching.
- **Output Characteristics (I\(_D\) vs V\(_{DS}\))**: Smooth current modulation with increasing V\(_G\) and V\(_{DS}\), indicating good output performance.
- **Mobility**: Field-effect mobility remains constant with increasing gate electric field, showing minimal scattering and high-quality interfaces in the 2D materials stack.

These results highlight the potential of 2D materials like MoS₂, graphene, and h-BN for scalable, high-performance transistor applications.
<img width="993" height="617" alt="image" src="https://github.com/user-attachments/assets/fc6ba45e-3e99-4392-9e1a-bae83cf59e8e" />

The diagram on the top left shows a non-planar transistor with key components:

- Gate: Controls the flow of current through the channel.
- Channel: Region where current flows between the source (S) and drain (D).
- Body: Underlying region connected to the substrate.
- STI (Shallow Trench Isolation): Insulates neighboring devices.

The biggest challenge is to form a single-crystalline semiconductors on a non-planar surface is difficult using conventional semiconductor fabrication techniques.
<img width="967" height="535" alt="image" src="https://github.com/user-attachments/assets/c08a8fed-1b87-4848-8d93-09cb12fce556" />

Single-Layer CMOS (a): This is the traditional CMOS design where NMOS and PMOS transistors are fabricated on a single silicon layer. Each transistor operates in the same planar layer, with devices connected laterally.

Monolithic 3D CMOS (b): In this design, NMOS and PMOS transistors are stacked in two separate layers, enabling higher density. The P-Channel (PMOS) is placed on top of the N-Channel (NMOS), separated by an oxide layer. This approach reduces the footprint and allows better performance due to shorter interconnects.

Single-Layer CMOS Logic (c): Shows logic gates (inverter, 2-input NAND, and 2-input NOR) built using traditional single-layer CMOS. Transistors are laid out horizontally, with interconnections taking more space.

Monolithic 3D CMOS Logic (d): Logic gates are constructed with two transistor layers (Layer 1 and Layer 2), reducing the area required for interconnections. Vertical integration improves performance and reduces delay by shortening signal paths.

<img width="951" height="514" alt="image" src="https://github.com/user-attachments/assets/a2545cfe-6666-4915-8355-7e78c0a0e359" />

**Dual Damascene Cu**, used for the 7nm technology node with a 36nm pitch, combines vias (vertical connections) and lines (horizontal connections) in a single patterning step. It relies on copper (Cu) for interconnections; however, as dimensions shrink, challenges such as gap filling and maintaining reliability become increasingly significant.

**Single Damascene Cu**, used for the 5nm technology node with a 28nm pitch, involves splitting the creation of vias (vertical connections) and lines (horizontal connections) into separate steps. This approach addresses the challenges of smaller dimensions, with a primary focus on reducing resistance (R) in both lines and vias to maintain optimal performance.

**Barrier and via metal optimization**, introduced at the 3nm technology node with a 20-24nm pitch, focuses on reducing the thickness of barrier layers (insulating layers) to minimize resistance while maintaining robust and reliable via connections. This optimization is essential to meet the performance and scaling demands of advanced nodes.

At sub-18nm pitch, **subtractive RIE** and alternative metals like ruthenium (Ru) are introduced to address the reliability and scaling challenges faced by traditional copper interconnects. Subtractive Reactive Ion Etching (RIE) enables more precise patterning of interconnects, while the use of Ru provides improved performance and durability at such advanced dimensions.

For future nodes with pitches below 15nm, **post-Damascene interconnects** featuring tall, barrier-less designs are envisioned. This approach enhances electromigration (EM) reliability, ensuring durable and robust connections despite the continued shrinking of dimensions, thereby addressing key challenges in advanced interconnect scaling.
<img width="962" height="502" alt="image" src="https://github.com/user-attachments/assets/085a8f40-ebb8-4c23-803b-9e06c9e82ccb" />

The image shows how a selective barrier, typically tantalum nitride (TaN), can improve copper interconnects in semiconductor manufacturing. This barrier reduces resistance, enhances reliability by preventing copper ion migration, and aids in controlling copper thickness. The process involves cleaning the copper surface, depositing TaN using atomic layer deposition (ALD), and removing sacrificial layers. This technique is crucial for advancing semiconductor technology and ensuring reliable, high-performance devices.

<img width="1000" height="547" alt="image" src="https://github.com/user-attachments/assets/c55024c6-85ef-4d7f-95c4-2d4bdd0912a4" />
**Back-Side Power Delivery Network (BS-PDN)**

In advanced semiconductor manufacturing, efficient power delivery is critical to the performance and reliability of integrated circuits. Traditional Front-Side Power Delivery Networks (FS-PDNs) often suffer from high IR-drop, which can limit device performance and reliability. To address this challenge, Back-Side Power Delivery Networks (BS-PDNs) have emerged as a promising solution.

BS-PDNs involve routing power supply rails on the backside of the chip, enabling shorter and wider power lines. This configuration significantly reduces IR-drop, leading to improved power delivery efficiency. As a result, BS-PDNs offer several advantages:

- Reduced IR-drop: Lower voltage drops across the power network, leading to improved performance and reliability.
- Decreased standard cell area: More efficient power delivery allows for smaller standard cell sizes.
- Improved performance: Lower IR-drop leads to faster switching speeds and reduced power dissipation.

By adopting BS-PDNs, semiconductor manufacturers can develop high-performance and energy-efficient integrated circuits that meet the demands of modern electronics.


</details> 

### 🚀 Project Overview

This project demonstrates a full RTL-to-GDSII physical design flow using OpenROAD of BabySoC.
The final output includes:

*Floorplan
*Placement
*Clock Tree Synthesis
*Routing
*SPEF (Standard Parasitic Exchange Format) extraction
*Post-route Static Timing Analysis

### MY PROJECT REPOSITORY LINK
This project was developed using GitHub Codespaces.

### 🔗 GitHub Repository: 
```bash
https://solid-space-disco-q7694rgvq7g9h9r4v.github.dev/
```


### **OpenROAD + noVNC Cloud Environment**

This repository launches a **ready-to-use GitHub Codespace** with OpenROAD tools, an XFCE desktop, and browser-based **noVNC** access.  
It is designed for testing and learning **physical design (PD) flows** in a cloud-based environment — without needing any local installation.

---
### 🧩What It Is

This repository provides a cloud-based environment (like GitHub Codespaces or VSCode in the browser) that runs:

OpenROAD tools – used for ASIC physical design automation (placement, routing, timing, etc.)

XFCE Desktop – a lightweight Linux desktop environment

noVNC – a browser-based remote desktop viewer

So, instead of installing OpenROAD locally, you can run and view it directly in your browser.
### 🔍 Why It’s Useful

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

### SPEF (Standard Parasitic Exchange Format) extraction
It is a file that contains parasitic extraction information of your routed design — mainly:
Resistance (R)
Capacitance (C)
Net connectivity
Parasitic nodes created after routing

SPEF is used for Post-Route Static Timing Analysis (STA) to get accurate timing numbers because after routing, wires have real RC delay.

### ✅ What SPEF Contains (Simple Explanation)

For each net in your design, SPEF stores:

*Total capacitance of the net
*Capacitance of each sub-node
*Resistances between wire segments
*Coupling capacitances between signals

Example small snippet:

```bash
*D_NET N1 0.025
*CAP
1 N1 0.010
2 N1 N2 0.015
*RES
1 N1 N1_1 50.0
2 N1_1 N2 40.0
```

### ✅ Why SPEF Is Important

After routing, wires create delay.
SPEF gives actual delays to STA tools like OpenSTA or PrimeTime.

Without SPEF → STA uses ideal wires → wrong timing.

With SPEF → Real RC delay → accurate timing report.

### 🚀 How to Generate SPEF in OpenROAD (exact steps)

You should be at post-route stage (detailed routing completed).

In the OpenROAD Tcl terminal, run:

1️⃣ Load your design (DEF + LIB + SDC)

Example:
```bash
read_lef tech.lef
read_lef stdcell.lef
read_def routed.def
read_liberty typical.lib
read_sdc design.sdc
```

2️⃣ Run the SPEF extraction

OpenROAD command:
```bash
estimate_parasitics -spef design.spef
```

OR, in newer flows:
```bash
write_spef design.spef
```
3️⃣ Verify SPEF was generated
```bash
report_parasitics
```

You will see resistance and capacitance values per net.

4️⃣ Use SPEF for Post-Route STA
```bash
read_spef design.spef
report_checks -path_delay max
report_tns
report_wns
```

Now STA will show real timing after routing.

### 🎯 Where to run the commands?

Run inside OpenROAD Tcl command window (terminal inside GUI or openroad executable in shell).

Not inside Linux terminal.
Inside OpenROAD only.


###  Post-Route STA
```bash
read_liberty tech/typical.lib
read_sdc constraints/design.sdc
read_spef results/design.spef

report_checks -path_delay max
report_tns
report_wns

```
 Understanding how the generated SPEF is used for post-route STA in real design flows.

-Developed an end-to-end understanding of how digital design data becomes a 
physical chip ready for timing closure and sign-off.


