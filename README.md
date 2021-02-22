<p align="center">
  <a href="" rel="noopener">
 <img width=350px height=200px src="https://i.imgur.com/PgdzSa8.png" alt="Docker logo"></a>
</p>

<h3 align="center">TICK stack docker-compose newest ver</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![Platform](https://img.shields.io/badge/platform-TICKstack-orange.svg)](https://www.influxdata.com/blog/introduction-to-influxdatas-influxdb-and-tick-stack/)
[![GitHub Issues](https://img.shields.io/github/issues/DHaiDang/TICK_stack_docker-compose.svg)](https://github.com/DHaiDang/TICK_stack_docker-compose/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/DHaiDang/TICK_stack_docker-compose.svg)](https://github.com/DHaiDang/TICK_stack_docker-compose/pulls)
[![License](https://img.shields.io/badge/license-InfluxData-blue.svg)](https://github.com/influxdata)

</div>

---

<p align="center"> 🤖 Hello I'm Dang

    <br> 
</p>

## 🎈 Usage <a name = "usage"></a>

```
$ git clone https://github.com/DHaiDang/TICK_stack_docker-compose.git
```

To use the docker-compose, type:<br>
Running background:

```
$ docker-compose up -d
```

### Check that InfluxDB works:

Run this curl command, if no errors occur InfluxDB is running:

    curl http://localhost:8086/ping

#### The `influx` client

Use the built-in influx cli service:

    docker-compose run influxdb-cli

### Check that Telegraf works

By default, the Telegraf creates a `telegraf` database.
Check that InfluxDB has such a database in addition to the `_internal` database.

    docker-compose run influxdb-cli
    > show databases

### Check that Chronograf works

Access the Chronograf inteface, [http://localhost:8888](http://localhost:8888)

### Check Kapacitor works

First, run this curl command, if no errors occur Kapacitor is running:

    curl http://localhost:9092/kapacitor/v1/ping


Use the built-in kapacitor cli service:

    docker-compose run kapacitor-cli
    $ kapacitor list tasks

Confirm Kapacitor is subscribed to all databases in InfluxDB

    docker-compose run influxdb-cli
    > show subscriptions

## 🎉 Acknowledgements <a name = "acknowledgement"></a>

- To learn about monitoring
- For working
- References
