# Cab Trip Chain Analysis
- Developed a robust model to identify multi-leg cab trip chains (3–4 or more linked seeks/offers) using graph-based analysis, trip duration optimization, and visual analytics in Python.
- Extracted, cleaned, and transformed over 5,000 cab operator trip records using pandas, ensuring consistency in datetime formats, location fields, and route mappings for accurate downstream processing.
- Standardized Seek and Offer date/time fields into datetime objects, enabling precise duration calculations and categorization into time-of-day buckets: Morning, Afternoon, Evening, and Night.
- Engineered derived fields such as:
- Up Trip: Seek Location → Seek Destination
- Down Trip: Offer Location → Offer Destination
- Trip Duration: Offer Time − Seek Time
These supported route efficiency analysis and chain detection.
- Identified duplicate routes by flagging identical combinations of Username + Route + Duration, helping surface operators who frequently posted overlapping or repeated trips.
- Applied group-based minimum duration logic to pinpoint the shortest available trips per route, optimizing match selection for both up and down directions.
- Modeled the dataset as a directed graph using NetworkX, where:
- Nodes represent locations
- Edges represent seek/offer trips
This enabled detection of multi-leg chains involving 3–4+ connected operators.
- Prioritized profitable chains by selecting paths that begin and end at strategically beneficial locations for the user, while simultaneously fulfilling multiple operators’ trip requests.
- Created visual insights using Matplotlib and Seaborn, including:
- Bar charts highlighting duplicate routes and shortest durations
- Network graphs visualizing detected multi-leg chains and operator connections
- Conducted operator-level analysis to spotlight frequent contributors such as Srinivas Rao, Ravi Kumar Thakur, and Sunil Kumar Singh, whose posts often formed part of viable trip chains.
- Delivered a final set of optimized “up–down” trip chains that:
- Maximize exchange fulfillment
- Minimize overall trip duration
- Enhance collaboration and efficiency among cab operators

## Technologies Used
- Python Libraries: pandas, datetime, networkx, matplotlib, seaborn
- Notebook Environment: Jupyter Notebook for graph modeling and visual reporting




