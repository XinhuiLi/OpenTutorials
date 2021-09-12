# C-PAC OpenTutorial

This repository holds resources for C-PAC OpenTutorial talk.

## QuickStart

### Step 1. Clone Repository
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
    fcpindi/c-pac:latest /bids_dataset /outputs participant
```

#### Useful Arguments
```
--pipeline_file <pipeline_config.yml>

--data_config_file <data_config.yml>

--preconfig <anat-only/benchmark-ANTS/benchmark-FNIRT/fmriprep-options/monkey/rodent>

--participant_label <participant label>

--save_working_dir
```

## Data Config
```
- anat: <anat data>
  func:
    run-1:
      scan: <func data 1>
    run-2:
      scan: <func data 2>
  site_id: site-none
  subject_id: sub-032167
  unique_id: ses-001
```

## Pipeline Config
Use text editor or [C-PAC GUI](https://fcp-indi.github.io/C-PAC_GUI/versions/nightly/browser/#/) to edit your pipeline config file. The [default config file](https://github.com/FCP-INDI/C-PAC/blob/master/dev/docker_data/default_pipeline.yml) can be used as a start point.

## For More Details
User documentation: https://fcp-indi.github.io
C-PAC forum: https://groups.google.com/forum/?utm_medium=email&utm_source=footer#!forum/cpax_forum
C-PAC GitHub: https://github.com/FCP-INDI/C-PAC