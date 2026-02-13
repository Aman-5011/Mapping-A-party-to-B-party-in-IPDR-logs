Mapping-A-party-to-B-party-in-IPDR-logs
Welcome to the Mapping A-party to B-party project! This is a comprehensive, multi-page web application designed to simplify the complex world of IP Data Records (IPDR).

By transforming raw, messy logs into a visual and interactive dashboard, this tool helps network analysts and security teams understand exactly who (A-party) is communicating with whom (B-party), what they are doing, and whether their behavior is suspicious.

#Key Features
1. Secure Access: A built-in authentication system (Login/Signup) with hashed passwords ensures that sensitive network data stays private.
2. Flexible Data Ingestion: Don't worry about rigid CSV formats. Our "Smart Mapping" interface lets you drag and drop your logs and manually tell the system which column is which.
3. Automated Data Enrichment: The app does the heavy lifting for you:
4. Geolocation: Sees where the A-party is located (Country, State, City).
5. Reverse DNS: Turns cryptic B-party IP addresses into recognizable domain names (e.g., 172.217.x.x becomes google.com).
6. Smart Metrics: Automatically calculates session durations and converts data volumes (Bytes to MB).
7. Interactive Analytics: Use the dashboard to filter by User ID, IP, or Date. Visualize the data through world maps and interactive charts (Top Websites, Data Usage, etc.).
8. ML-Powered Anomaly Detection: We've integrated a Scikit-learn Isolation Forest model. It scans your logs to find "outliers"—those rare, weird connections that might indicate a security breach or network fault.
9. Privacy Management: Easily view uploaded file history and delete specific datasets to keep the database clean and compliant.

#Technological Stack
Category,Tools Used
Language,Python 3.x
Web Framework,Streamlit
Data Processing,"Pandas, NumPy"
Database,SQLite (SQLAlchemy)
Visualizations,"Plotly, Matplotlib"
Machine Learning,Scikit-learn (Isolation Forest)
External APIs,Ipinfo.io (for Geolocation)

#How it Works: The Workflow
Login: Access your secure workspace.

Upload & Map: Drop your IPDR CSV file into the "Upload" page. Map your headers to our standard fields (Source IP, Destination IP, Data, etc.).

Process: The system enriches the data (DNS lookups + Geolocation) and saves it to a central SQLite database.

Explore: Use the "Search Data" page to filter through millions of records and see the "A-party to B-party" relationship visualized on maps and graphs.

Detect: Run the Anomaly Detection tool to let AI flag suspicious activity for you.

Manage: Use the management tab to clear old logs or review your upload history.
