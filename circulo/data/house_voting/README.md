## Congress Voting Data

The data can be found at <https://www.govtrack.us/developers/data>

## Description
Congress voting records from 2014.

Directed: No

Weighted: Yes

Multigraph: No

### Vertices 
Each vertex represents a congressperson for whom we have voting data.

Attributes:
* **name**: Unique identifying id
* **full_name**: Name of the congressperson
* **state**: State represented
* **id**: Unique identifier. In most cases, use "name."
* **party**: Political party.

### Edges
There is an edge between two nodes whenever the congresspeople vote together on an issue. The edges are weighted by the number of votes that are shared. 

Attributes:
* **weight**: The number of times the congresspeople on each side of this edge have voted the same way.

## Ground Truth
`get_ground_truth` returns a VertexClustering grouped by the parties of the politicians.

## Other Notes
* See `run.py` for specific details

## References
Thanks to GovTrack.us
