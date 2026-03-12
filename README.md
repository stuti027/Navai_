STEPS TO RUN:
1. Create a Virtual Environment
    python -m venv venv
2. Activate the Virtual Environment
    Windows:
        venv\Scripts\activate
    Mac / Linux:
        source venv/bin/activate
3. Install Dependencies
    pip install -r requirements.txt
4. Run Route Optimization
    python src/astar.py <source_node> <destination_node> 
    (nodes: A, B, C, D or E)
    Example:
    python src/astar.py A C