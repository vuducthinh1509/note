# note

# Initial Connection
To connect for the very first time you must call register first:
1. Register the client warp-cli register.
1. Connect warp-cli connect.
1. Run curl https://www.cloudflare.com/cdn-cgi/trace/ and verify that warp=on

# Generate UE
Generate multiple UE use bash script
```
#!/bin/bash

# Create folder to save yaml file (does not exist)
mkdir -p ue-list

# Use loop to create yaml file 
for i in {1..10}   # 10 is the number of yaml file
do
    ./bin/ue-gen -c config/uegen.json -p "ue-list/ue_$i.yaml"
done
```

# How to import json file to MongoDB
