### 缺陷 

Generally S3 cannot offer the same performance or semantics as a local file system. More specifically:
random writes or appends to files require rewriting the entire filemetadata operations such as listing 
directories have poor performance due to network latencyeventual consistency can temporarily yield stale 
data(Amazon S3 Data Consistency Model)no atomic renames of files or directoriesno coordination between multiple 
clients mounting the same bucketno hard linksinotify detects only local modifications, not external 
ones by other clients or tools