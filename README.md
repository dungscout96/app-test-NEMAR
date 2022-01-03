# app-test-NEMAR
Example NEMAR pipeline

To test:
```
git clone https://github.com/dungscout96/app-test-NEMAR.git
cd app-test-NEMAR
./main
```

The pipeline runs on a Docker container via Singularity. 

## Files
- `main`: the entrypoint script
- `config-dataqual.json`: specifying path to BIDS dataset on and datasetID
- `bids_dataqual.m`: main pipeline script

## Docker execution

A simple docker application running Octave and some EEGLAB scripts. See also an older project https://github.com/sccn/nemar_tool_proof_of_concept

Usage
```
$ docker build --tag=octavedock13 .
$ docker run --rm -it octavedock13
$ # Then at the Octave prompt, install the signal processing toolbox (this should really be done in the Docker file)
$ pkg install -forge control
$ pkg install -forge signal
$ pkg load signal
$ # Then run script
$ ./main
```

Run the script file directly (for a modified version that would include the signal processing toolbox)

```
$ docker run --rm -it octavedock script_test.m arg1  # Run the example file
```
