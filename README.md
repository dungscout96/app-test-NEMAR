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
