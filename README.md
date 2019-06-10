# SDM-RDFizer


Create the Docker Container

```
docker build -t rdfizer .
```

Run the Application

```
docker run -d --name rdfizer rdfizer
```

Execute mapping
```
docker exec -it rdfizer /app/run.sh /app/mappings/config.ini
```

## Example of a Config file

```
[default]
main_directory: /home/guillermobet/Documentos/Fraunhofer/ProjectIASIS/SemanticEnrichment

[datasets]
number_of_datasets: 1
output_folder: ${default:main_directory}/graph

[dataset1]
name: ADSampleDataWP4CO
format: csv
path: ${default:main_directory}/data/csv/ADSampleDataWP4CO.csv
mapping: ${default:main_directory}/mappings/AD_CO.ttl
remove_duplicate_triples_in_memory: yes
```
