pip install streamlit yfinance pandas
streamlit run radar.py
Act as a Principal Quantitative Systems Architect and Full-Stack Python Developer. Rebuild the application into an ultra-high-frequency, production-grade trading terminal named "G2I Big-Bull Order Flow & Speed Radar v3.0". 

The core objective is to track live institutional market orders and liquidity frequency directly from the NSE tick data streams to catch immediate Big Bull entries within a strict 2-second processing window, ignoring standard misleading broker retail percentages.

### Core Architecture & Technical Requirements:

1. Ultra-High-Frequency (UHF) Data Pipeline:
   - Configure a parallelized data worker using Streamlit state management and high-frequency `yfinance` fetches optimized for 1-minute intervals.
   - Implement an aggressive 2-second auto-refresh and execution cycle using a continuous asynchronous loop (`time.sleep(2)` with dynamic state reruns).
   - Expand the scanning universe dynamically to evaluate all highly liquid NSE Small-Cap, Mid-Cap, and momentum-driven equities continuously.

2. Advanced Multi-Factor Institutional Filters (New Guardrails):
   - Real-Time Order Flow Tracking: Calculate immediate order book velocity where current 2-second volume exceeds the 20-period moving volume average by 300%+.
   - VWAP Confluence Filter: The system must dynamically verify that the current market price is trading strictly ABOVE its Volume Weighted Average Price (VWAP) to ensure institutional buying support before generating a signal.
   - Circuit Proximity Warning: Track the exchange-defined Upper Circuit limit. If a high-flying small-cap is within 1.5% of its daily circuit limit, flag it as "🔒 CIRCUIT RISK - DO NOT ENTER" to protect capital from liquidity traps.

3. Dual-Zone Asymmetric Dashboard UI Layout:
   - Upper Dashboard (Deep Intelligence Radar): This block remains inactive or neutral until a user clicks on an active stock card below. Once clicked, it instantly parses the metadata of that specific stock, rendering critical metrics: Institutional Entry Zones, Day High proximity, and a mathematically projected dynamic target/stop-loss matrix.
   - Lower Dashboard (High-Speed Stock Suggester): A clean, multi-column matrix updating every 2 seconds displaying: Ticker, Spot Price, Speed Velocity Index (e.g., ⚡ 7.4x), and an interactive "Analyze 🎯" button that hooks into the Upper Dashboard state.

4. Tactical Live Chatbot & Real-Time Commentary:
   - Implement an autonomous, zero-noise "AI Tactical Feed" container. Based on live mathematical calculations, it must print instant, single-line institutional trade logs (e.g., "[11:24:02] 🚨 INSTITUTIONAL PUMP: Massive block inflow detected in [Ticker]. Velocity accelerating.").
   - Integrate native browser-level Text-To-Speech (TTS) via the JavaScript Web Speech API. When a stock breaks past a 90% Confluence Probability, the system must broadcast an instant voice alert (Indian accent, 0.9x speed) to allow immediate screen-off execution.
   - Ensure a robust data fallback script that simulates volatile, high-momentum NSE price streams based on real historical breakout architectures if exchange APIs face connection lag.
   - 
