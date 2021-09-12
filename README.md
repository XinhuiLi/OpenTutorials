# C-PAC OpenTutorial Cheatsheet

### Step 1. Clone repository
```
git clone https://github.com/XinhuiLi/OpenTutorial.git
```

### Step 2. Pull C-PAC
```
docker pull fcpindi/c-pac:latest
```

### Step 3. Run C-PAC
```
docker run -i --rm \
    -v /Users/You/OpenTutorial/data:/bids_dataset \
    -v /Users/You/output_folder:/outputs \
    -v /Users/You/config_folder:/configs \
    -v /tmp:/scratch \
    fcpindi/c-pac:latest /bids_dataset /outputs participant --pipeline_file /configs/pipeline_config.yml
```