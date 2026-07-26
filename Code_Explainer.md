📘 Code Explainer: Full-Stack Multi-Agent Stream Processor

This document breaks down the interactive frontend layout and runtime mathematical logic line-by-line for technical interviewers.

1. Architectural Full-Stack Stream Processing

if "system_stream_db" not in st.session_state: Implements state persistence inside a web layer. Instead of reading stagnant historical database files from disk, this function spins up a transient, live in-memory telemetry router to simulate real-time processing loads.
st.metric(...) / st.sidebar.selectbox(...): Deploys responsive full-stack elements natively via Python. This formats raw backend dictionary variables directly into interactive web objects, metric data cards, and real-time filtering widgets.
2. Algorithmic Multi-Agent Evaluation (The Onyx Agent Logic)

df_stream["Z_Score"] = (df_stream["Latency_MS"] - mean_latency) / std_latency: This is the heart of the Onyx Agent's processing matrix. It continually calculates rolling standard deviations and averages across the live data stream, computing Z-scores to pinpoint non-linear performance anomalies.
np.where(df_stream["Z_Score"] > 2.5, ...): Establishes our live operational circuit-breaker boundary. If any microservice requests spike past 2.5 statistical deviations from the cluster average, the Onyx Agent automatically intercepts the request ID, overrides the system state flag, and isolates the anomaly.
