# BIDS Organizer Tool (dcm2bids_c)

This tool organizes medical imaging data into the Brain Imaging Data Structure (BIDS) format. It's designed to simplify the process of converting and organizing DICOM files and other associated data into the BIDS standard, converting also dicom (DCM) data in nifti (nii) files and nii files in mif (mrtrix3) files. 
It requires a path for the sourcedate raw folder to convert. The optional flags are useful to change sub_id and output (derivatives) path without changing the config.json file (assuming that the anat and dwi folders in the config.json file are set correctly).

## Features

- Organize anatomical, diffusion-weighted, functional, TMS, and behavioral data into the BIDS structure.
- Command-line interface for easy integration into workflows.
- Support for custom configuration via JSON files.
- Error handling to ensure compliance with BIDS standards.

## Prerequisites

- [jq](https://stedolan.github.io/jq/)
- [dcm2niix](https://github.com/rordenlab/dcm2niix)
- [mrconvert](https://mrtrix.readthedocs.io/en/latest/reference/commands/mrconvert.html) from MRtrix3

## Usage

```bash
dcm2bids_c /path/to/data_directory --config ./myconfig.json
```

### Arguments:

- `--config | -c` : Specify the path to your configuration JSON file. (Default: `./config.json`)
- `--id | -i` : Specify the subject ID. Overrides the ID from the configuration file if provided.
- `--out | -o` : Specify the output (derivatives) folder.
- `--help | -h` : Show usage.
