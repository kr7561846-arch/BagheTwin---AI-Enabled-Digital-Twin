BagheTwin: AI-Enabled Digital Twin for CSS and SRP Operations

LINK FOR THE DASHBOARD: https://baghetwin-ai-enabled-digital-twin.onrender.com

 **Please find the prototype demonstration video in the uploaded files.**

OVERVIEW
BagheTwin is an AI-enabled 3D Digital Twin built for the heavy oil wells of the Baghewala Field in Rajasthan, operated by Oil India Limited (OIL). It gives operators one dashboard to monitor, diagnose and optimize the whole well-to-surface system: Cyclic Steam Stimulation (CSS), the Sucker Rod Pump (SRP) and the surface storage tank.

THE PROBLEM
Baghewala's crude oil is thick and does not flow easily. Steam is injected through CSS to heat the oil, and the SRP then lifts it to the surface and into a storage tank. From there it is transported to the IOCL Koyali Refinery in Gujarat. Today, unplanned pump and steam-line failures cause production loss, and remote wells are monitored manually.

OUR SOLUTION
BagheTwin is a live 3D replica of the CSS, SRP and tank system. It compares real-time steam and pump data against healthy baselines, detects abnormal behaviour early, and suggests adjustments to steam volume, steam pressure, soak time and pump speed.

It models the real physical chain:
- Low steam quality -> heavy oil viscosity -> high pump load -> low tank inflow
- High steam quality -> low oil viscosity -> low pump load -> high tank inflow

WHAT MAKES IT DIFFERENT
1. One 3D twin of CSS, SRP and the tank together, showing which part has a problem and how it affects the others.
2. The AI learns normal behaviour only (LSTM-Autoencoder), so it can warn early without any past failure data, and it shows which sensor caused the anomaly.

HOW IT WORKS
1. Data Collection: Existing field sensors send vibration, temperature, pressure, rod load and tank level through SCADA.
2. Data Layer: FastAPI and MySQL validate, clean and synchronize the real-time series data.
3. Digital Twin: A 3D model built in Blender and rendered with Three.js stays synced with live data.
4. AI Analytics: A PyTorch LSTM-Autoencoder learns normal operation, gives an anomaly score, and identifies the fault type and contributing sensor.
5. Optimization: Suggests steam volume, pressure, soak time and SPM settings to lower the steam-oil ratio while maximizing oil output per cycle.
6. Visualization: A React dashboard shows live values, 3D twin status, fault alerts and tuning suggestions.

DASHBOARD FEATURES
- Live sensor readings for CSS, SRP and production in one view
- Interactive 3D twin (pumping unit, wellhead, rod string, reservoir, subsurface pump, storage tank)
- AI fault detection with anomaly score, plus Normal and Simulate Fault modes
- Component and equipment health status
- Operating optimization suggestions
- Trend charts for temperature, pressure, vibration and production


