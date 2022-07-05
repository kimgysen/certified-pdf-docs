==========
Monitoring
==========

Production setup requires professional monitoring of general metrics, and to prevent / be notified about possible failures. This includes both metrics about the Java processes (JVM monitoring), but also custom metrics.
Influx / Grafana are commonly used for this purpose.

.. image:: img/influx_grafana.png
  :width: 800
  :alt: influx_grafana

By using the Java Micrometer library, our Java processes will send metrics to an Influx Database (using HTTP Post).
Grafana is a dashboarding tool that allows for visualising graphical diagrams based on these metrics.
It also allows us to define thresholds and automated alerting (for example through email) when thresholds have been (b)reached.
