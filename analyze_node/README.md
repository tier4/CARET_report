# Scripts to create node analysis reports

## What is created

- Path analysis report
  - This report shows detailed information of each callback function
    - Metrics: Frequency, Period and Latency
    - Statistics and graph (timeseries and histogram)
  - It is useful for each package developers, also to investigate a problem
- Artifacts
  - `report_ooo/node/{package_name}/`
    - `index.html` : report main page
    - `ooo.html` : graph file as html
    - `ooo.png` : graph file as image
    - `stats_node.yaml` : statistics file

## Scripts

### `analyze_node.py`

```sh:usage
usage: analyze_node.py [-h] [--package_list_json PACKAGE_LIST_JSON] [-s START_POINT] [-d DURATION] [-f] [-v]
                       trace_data

```

- This script creates detailed information of each callback function:
  - Timeseries graph and histogram graph (html and image files)
  - statistics file (`stats_node.yaml`)

### `make_report_node.py`

```sh:usage
usage: make_report_node.py [-h] report_directory
```

- This script creates a report html page
