# Ex No: 01 - Design & Implementation of CMOS Inverter Design Using Cadence EDA Tools

## Aim
To design and implement a CMOS inverter circuit using Cadence EDA tools, analyze its electrical characteristics, and understand the fundamental principles of CMOS technology, including the design process, layout, and simulation techniques.

## Tools Required
- Personal Computer
- Cadence Virtuoso Software

## Schematic Simulation - Procedure for Creating the Schematic Simulation

### Commands to Get into Cadence
1. Right-click and open the terminal window.
2. Type the following commands and press enter:
   ```sh
   csh
   source /cadence/install/cshrc
   virtuoso
   ```
3. Two windows must open:
   - **Virtuoso/Command Interpreter Window (CIW)**
   - **“What’s New…” Window** (Close this window)
4. Use the Virtuoso CIW window for further processing.

### Steps for Schematic Simulation using Cadence
1. **Create a New Library**
   - Go to `File → New → Library`
   - Name the library (e.g., `VLSILAB_EXP_1`).
   - Enable `Attach to an existing technology library`, click OK.
   - Attach the library to `gpdk045`, then click OK.

2. **Create Schematic Cell View**
   - Open the Virtuoso CIW window.
   - Navigate to `File → New → Cell View`.
   - Set up the new file:
     - **Library:** Select the one you created.
     - **Cell:** Name the experiment (e.g., `Inverter_ViewSchematic`).
     - **Type:** `Schematic`, then press OK.
   - Add required components from the libraries and make connections:
     - Use the shortcut key `I` to insert instances.
     - Click `Browse` to open the library browser.
     - Select components from `gpdk045` (e.g., `nmos1v`, `pmos1v`).
     - Create input and output pins.
     - Make connections using the fixed narrow wire key.
     - Click `Check and Save`.
   
   ![Exp1_vlsi_1](https://github.com/user-attachments/assets/b2d6e421-8e3a-4120-9afc-0864a2d90f85)

3. **Creating the Symbol for Schematic Cell View**
   - In the schematic window, execute:
     - `Create → Cell View → From Cell View`
     - Ensure that the Library Name, Cell Name, and View Name match the schematic, then press OK.
   - The Symbol Generation form appears. Click OK if no changes are needed.
   - A new window with a default symbol is created.
   - Edit the symbol if necessary or continue.
   - Execute `Create → Cell View → From Cell View`.
   - Ensure the Library Name and Cell Name match those used for the schematic, then press OK.
   - Check the pin positions and press OK.
   - Modify the shape using `Create → Shape → Choose required options to edit`.

   ![image](https://github.com/user-attachments/assets/e947dcda-b023-4668-a955-a5faf0949702)

4. **Creating the New Test Cell View**
   - Go to the CIW window and execute `File → New → Cell View`.
   - Set up the new file:
     - **Library:** Select the one you created.
     - **Cell:** Name it differently from the schematic cell view (e.g., `Inverter_test`).
     - **View:** `Schematic`.
     - **Type:** `Schematic`, then press OK.
   - Follow Step 2 to make the required connections.

   ![image](https://github.com/user-attachments/assets/0f1eb390-537e-4915-a9d5-6855883745d4)

### Analog Simulation by Spectre
1. In the test cell view window:
   - Launch `ADE L (Analog Design Environment)`.
   - Execute `Setup → Simulation/Directory/Host`.
   - Set the simulation window to Spectre and click OK.
   - Execute `Analysis → Choose`, select the type, set specifications, and press OK.
   - Execute `Outputs → To Be Plotted → Select on Schematic`.
   - Select the **Input Wire (Vin)** and **Output Wire (Vout)** from your test schematic using the mouse.
   - Execute `Simulation → Netlist and Run`.

   ![Exp1_vlsi_2](https://github.com/user-attachments/assets/bfeedd79-f84b-44c3-963d-6bd5c84227c3)

### Transient Analysis Settings and Output

![exp1_vlsi_3](https://github.com/user-attachments/assets/0b82789e-eb03-42cb-9053-c23d2d47f7ed)

![exp1_vlsi_4](https://github.com/user-attachments/assets/ecaf633f-96a3-4628-b89e-e453beb164cc)

### DC Analysis Settings and Output

![image](https://github.com/user-attachments/assets/0ee74107-e03a-4204-b685-83ced611c993)

![image](https://github.com/user-attachments/assets/e6b8b6c7-378f-449e-82a5-72286f238b02)

## Results
1. Successfully designed the CMOS inverter schematic using Cadence EDA tools.
2. The simulation results demonstrated the correct logic operation of the inverter, where the output voltage switches between high (`Vdd`) and low (`0V`) levels, corresponding to the input voltage transitions.
3. The Voltage Transfer Characteristic (VTC) curve was plotted, showing the relationship between input and output voltages.












