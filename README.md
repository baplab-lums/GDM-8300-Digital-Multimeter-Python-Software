# GDM-8300 Data Logger & Visualizer

This Python-based Jupyter Notebook app allows you to connect to one or two **GW Instek GDM-8300 multimeters** via USB (VISA interface), read measurements continuously, plot them in real time, and automatically save the results in Excel, CSV, or JSON formats.

---

## 🧰 Features

- ✅ Connect to **1 or 2 GDM-8300** instruments via VISA
- ⏱️ Configure read interval and number of readings
- 📡 Send any SCPI command (e.g., `READ?`, `MEAS:VOLT:DC?`)
- 📊 Real-time **live plotting**
- 🧮 Automatic **difference calculation** (in dual-device mode)
- 💾 **Auto-save** after reading to Excel, CSV, or JSON
- 🧠 Built with `pyvisa`, `ipywidgets`, `matplotlib`, `pandas`

---

## Install required packages
Make sure you're using a Python environment with Jupyter installed.

pip install -r requirements.txt

Or manually:

pip install pyvisa ipywidgets pandas matplotlib openpyxl
Note: For USB instruments, we recommend NI-VISA

![image](https://github.com/user-attachments/assets/ed7def5e-dd48-4369-93dd-dd65f216f772)


## 📓 Usage

1. Launch Jupyter Notebook or Lab
2. Open `GDM8300_Logger.ipynb`
3. Select:
   - One or Two Device Mode
   - VISA resource(s) (e.g., `USB0::...::INSTR`)
   - SCPI command (default: `READ?`)
4. Press **Start** to begin logging

Results will be auto-saved at the end in your chosen format


## 📁 Output Format

| Timestamp           | Device 1 | Device 2 | Difference |
|---------------------|----------|----------|------------|
| 2025-04-16 12:30:00 | 0.1532   | 0.1201   | 0.0331     |

*(In single-device mode, only Device 1 readings are logged.)*

---

## 📃 License

MIT License — feel free to fork, improve, or adapt.

---

## 🙌 Acknowledgments

Built for lab data logging by Haris Hassan.  
Contributions welcome!
