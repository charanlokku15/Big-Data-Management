# Process for Wiki-Vote Graph Analysis

Step 1: Data Loading
Input File: Load the dataset from /FileStore/tables/Wiki_Vote.txt.

Format: Each line represents a directed edge in the format src (source node) → dst (destination node).

Step 2: Data Preparation
Parse Data: Extract source (src) and destination (dst) nodes from each line.

Create DataFrame: Structure the data into a DataFrame with columns src and dst.

Step 3: Graph Construction
Vertices: Identify all unique nodes (vertices) from the src and dst columns.

Edges: Use the src and dst pairs to define directed edges.

Build Graph: Construct a directed graph using the vertices and edges.

Step 4: Graph Analysis
Compute Degrees:

In-Degree: Count incoming edges for each node.

Out-Degree: Count outgoing edges for each node.

PageRank: Calculate PageRank scores to identify influential nodes.

Connected Components: Detect strongly connected components (SCCs) in the graph.

Community Detection: (Optional) Use algorithms like Louvain to find communities.

Step 5: Results Extraction
Sort Nodes: Order nodes by descending degree or PageRank score.

Top Nodes: Identify the top nodes with the highest degrees or PageRank.

Save Output: Write results to /FileStore/tables/output_3_2.txt.

Step 6: Output Interpretation
Influential Nodes: Nodes with high degrees or PageRank are key influencers.

Network Structure: Analyze SCCs and communities to understand sub-structures.

Notes:
Ensure the environment supports Spark and GraphFrames.

Adjust file paths as needed for your setup.