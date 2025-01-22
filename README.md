<h1 align="center">Monitoring :tada:</h1>

This repository provides an example of general monitoring using Grafana and Prometheus, as well as specific monitoring for machine learning with an example notebook demonstrating how to use Evidently AI.

## Installation

There are only one prerequisites:

* [Docker](https://docs.docker.com/get-docker/)

Having both, you'll need to clone the repository:

``` bash
git clone https://github.com/jeremy-vangansberg/simplon-monitoring.git
```

## Usage

### Monitoring Base

To run the monitoring setup for the FastAPI application, navigate to the `monitoring-base` directory and run the docker containers:

``` bash
cd monitoring-base
docker-compose up
```

Now you have access to those three containers and their respective ports:

* Prometheus: http://localhost:9090/
* Grafana: http://localhost:3000/
* FastAPI: http://localhost:8000/

On the FastAPI, you can access the `/metrics` endpoint to see the data Prometheus is scraping from it.

### Monitoring ML

The `monitoring-ml` folder contains additional monitoring resources and Jupyter notebooks for machine learning monitoring. To explore these resources, navigate to the `monitoring-ml` directory:

``` bash
cd monitoring-ml
```

You can open and run the Jupyter notebooks such as `test_demo.ipynb` to explore the monitoring capabilities for machine learning models. The notebooks demonstrate how to use `evidently` to generate and track metrics for machine learning models.

To install the required dependencies for the notebooks, run:

``` bash
pip install -r requirements.txt
```

## References

* [Prometheus FastAPI Instrumentator](https://github.com/trallnag/prometheus-fastapi-instrumentator)
* [Generate and Track Metrics for Flask API Applications Using Prometheus and Grafana](https://medium.com/swlh/generate-and-track-metrics-for-flask-api-applications-using-prometheus-and-grafana-55ddd39866f0)
* [PromQL for Humans](https://timber.io/blog/promql-for-humans/)