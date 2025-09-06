# Cab Trip Chain Analysis

- This project developed a model to identify multi-leg cab trip chains (3–4+ linked seeks/offers) by cab operators using advanced graph analysis, trip duration optimization, and visual analytics in Python.

- Extracted, cleansed, and transformed 5,000+ cab operator trip records using Python (Pandas), ensuring consistency in datetime formats, location fields, and route mapping for downstream analysis.

- Converted Seek/Offer Date & Time into standardized datetime objects, enabling accurate trip duration calculations and time-slot categorization (Morning, Afternoon, Evening, Night).

- Designed new derived fields including Up Trip (Seek Location → Destination), Down Trip (Offer Location → Destination), and Trip Duration (Offer–Seek) to support chain detection and route efficiency analysis.

- Conducted duplicate route detection by flagging identical Username + Route + Duration records, helping to identify operators frequently posting overlapping trips.

- Implemented shortest trip identification using group-based minimum duration logic, delivering optimal matches per up-trip and down-trip route.

- Modeled trips as a directed graph using NetworkX, where nodes = locations and edges = seek/offer trips, enabling detection of multi-leg trip chains with 3–4+ linked operators.

- Detected viable profitable chains by prioritizing paths that start/end at beneficial locations for the user, while fulfilling multiple operators’ requests in a single route.

   1.Developed visual insights using Matplotlib & Seaborn.

   2.Bar charts for duplicate routes & shortest durations.

   3.Network graph visualizations of detected multi-leg chains.

- Delivered operator-level analysis, highlighting key contributors such as Srinivas Rao, Ravi Kumar Thakur, and Sunil Kumar Singh, who frequently posted matching trips and formed part of multi-leg routes.

- Produced a set of optimized “up–down” trip chains that maximize exchange fulfillment, minimize trip duration, and enhance operator collaboration.

## Technologies Used

Python: pandas, datetime, networkx, matplotlib, seaborn

Jupyter Notebook:  graph-based modeling, visual reporting



