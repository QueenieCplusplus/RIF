# RIF
Routing Information Field

# Structur

Routing information is stored in the header of token ring frames in the RIF.


         +---------------+------------------+------------------+------
         | Route Control | Route Designator | Route Designator | ...
         +---------------+------------------+------------------+------
         
                 |                                        |
                 |                                        |
                 |                                        |
                 V                                        |
                                                          |
    +-----------+--------+-----------+---------------+    |
    | Broadcast | Length | Direction | Largest Frame |    |
    +-----------+--------+-----------+---------------+    |
       |                                                  |
       |                                                  |
       |                                                  |
       |                                                  V
       |                                      +----------+------------+
       |                                      | Ring Num | Bridge Num |
       |                                      +----------+------------+
       V
    +-----+-----------------------+
    | 000 | Specific Rout         |
    +-----+-----------------------+
    | 100 | All Routes Broadcast  |
    +-----+-----------------------+
    | 110 | Single Route Broadcast|
    +-----+-----------------------+
