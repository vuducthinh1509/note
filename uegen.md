# Generate UE
Generate multiple UE use bash script
```
#!/bin/bash

# Create folder to save yaml file (does not exist)
mkdir -p ue-list

# Use loop to create yaml file 
for i in {1..10}   # 10 is the number of ue configuration
do
    ./bin/ue-gen -c config/uegen.json -p "ue-list/ue_$i.yaml"
done
```