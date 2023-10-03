# Sample Queries

## File Format

The queries are stored in a CSV file with the following format:
* `8*n` rows where `n` is the number of queries
* Every 8 rows corresponds to a single query
* Each row corresponds to a vertex's position and the Boolean ground truth
* The order of the rows is:
    * Edge-edge queries: `ea0_t0, ea1_t0, eb0_t0, eb1_t0, ea0_t1, ea1_t1, eb0_t1, eb1_t1` where `a` or `b` indicates which edge, `0` or `1` indicates the endpoint of the edge, and `t0` or `t1` indicates the starting or ending positions of the edge.
    * Vertex-face queries: `v_t0, f0_t0, f1_t0, f2_t0, v_t1, f0_t1, f1_t1, f2_t1` where `v` indicates the vertex, `f0`, `f1`, or `f2` indicates the face vertices, and `t0` or `t1` indicates the starting or ending positions of the vertex.
* `7` columns of integers where the last column is either `0` or `1` for the boolean ground truth
* Each pair of columns (`1`/`2`, `3`/`4`, and `5`/`6`) comprise a single rational number for the `x`, `y`, and `z` coordinates of the vertex, respectively.
