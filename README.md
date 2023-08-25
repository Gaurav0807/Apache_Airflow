# Weather Data Fetcher using Apache Airflow

This project demonstrates how to use Apache Airflow to fetch weather data for multiple cities from an API, sort the data, and store it in a CSV file.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Usage](#usage)
- [DAG Configuration](#dag-configuration)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

- Python 3.x
- [Apache Airflow](https://airflow.apache.org/docs/apache-airflow/stable/start.html) installed

## Setup

1. Clone this repository:

    ```bash
    git clone https://github.com/yourusername/weather-data-fetcher.git
    cd weather-data-fetcher
    ```

2. Install required packages:

    ```bash
    pip install requests pandas apache-airflow
    ```

3. Obtain an API key from [OpenWeatherMap](https://openweathermap.org/api) and replace `"YOUR_API_KEY"` in `weather_data_dag.py` with your actual API key.

## Usage

1. Start your Airflow web server and scheduler:

    ```bash
    airflow webserver -D
    airflow scheduler -D
    ```

2. Access the Airflow UI in your browser (default: http://localhost:8080).
   
3. Trigger the "weather_data_dag" manually or set the desired schedule interval.

## DAG Configuration

In the `weather_data_dag.py` file, you can configure:

- `start_date`: The date from which the DAG starts running.
- `schedule_interval`: The interval at which the DAG is executed (e.g., `'@daily'`).
- `api_key`: Replace with your OpenWeatherMap API key.
- `cities`: Add or modify the list of cities for which you want to fetch weather data.

## Contributing

Contributions are welcome! If you find any issues or improvements, feel free to open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
