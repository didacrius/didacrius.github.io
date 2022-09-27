---
layout: post
title:  "Grafana con Tempo, Prometheus y Loki en Docker"
author: didac
categories: [ Observabilidad, Monitoring ]
tags: [ OpenTelemetry, Datadog ]
image: assets/images/post-headers/grafana-tempo-loki-prometheus.png
excerpt: "¿Cómo configurar Grafana para conectar con Tempo, Prometheus y Loki y correlacionarlos?"
description: "¿Cómo configurar Grafana para conectar con Tempo, Prometheus y Loki y correlacionarlos?"
featured: false
hidden: false
beforetoc: "En esta entrada veremos cómo conectar Grafana a los diferentes datasources de Tempo, Prometheus y Loki y cómo correlacionarlos entre ellos."
toc: true
audio: "/assets/audio/post1.mp3"
---

En esta entrada veremos cómo tener Grafana pre-configurado con Tempo, Prometheus y Loki en Docker. También veremos de manera muy breve qué nos solución nos ofrecen los diferentes servicios, anteriormente citados, de los que Grafana sacará esa información.

## Grafana
### ¿Qué es Grafana?
Grafana es uno de los mejores y más completos servicios de monitoring de código abierto, Open Source, donde podemos tener una UI amigable a la vez que poder explotar los datos de las diferentes verticales de la observabilidad, trazas, métricas y logs, desde un mismo punto centralizado y poder correlacionar dichas verticales entre ellas para tener una buena base para la observabilidad de nuestro sistema.
### ¿Cómo añadir Grafana en Docker?
Datadog tiene un exportador para el OTEL Collector, lo podemos encontrar en el repo de contribuciones de OTEL Collector "otel-contrib (meter el link)".

Para poder exportar la telemetría de la vertical trazas del protocolo de Open Telemetry a Datadog a través del OTEL Collector tendremos que añadir un nuevo exportador, el de Datadog, en nuestro fichero de configuración de OTEL Colector para posteriormente añadirle Datadog en la pipeline de trazas que nos interese de nuestro mismo archivo de OTEL Collector.

## Tempo
### ¿Qué es Grafana Tempo?
Grafana Tempo es un servicio, altamente escalable y de código abierto, de ingesta de trazas distribuidas. Puede ingerir métricas de gran variedad de protocolos, sobre todo los de código abierto como OpenTelemetry. Tiene una gran integración con Grafana, Prometheus y Loki.

### ¿Cómo añadir Grafana Tempo en Docker?
Work in progress.
- Añadir en docker.
- Archivo configuración.

## Prometheus
Prometheus es un servicio de ingesta de métricas.
### ¿Qué es Prometheus?
Prometheus es un agregador de métricas. Prometheus tiene la peculariadad respecto a los demás servicios, Tempo y  Loki, que usa un sistema pull para la ingesta de métricas es decir que en vez de que los servicios envíen, sistema push, las métricas a Prometheus es Prometheus quien pregunta por las métricas, scrapping, cada cierto tiempo periódicamente.


### ¿Cómo añadir Prometheus en Docker?
Work in progress.
- Añadir docker.
- Archivo de configuración.

## Loki
### ¿Qué es Grafana Loki?
Grafana Loki es un servicio de ingesta de logs. Entre sus características destacan que se trata de un servicio escalable horizontalmente y, por lo tanto, de alta disponibilidad. Tiene una gran integración con Grafana, Tempo y Prometheus.

### ¿Cómo añadir Grafana Loki en Docker?
Work in progress.
- Añadir docker.
- Archivo de configuración.

## Conectar Grafana con datasources
### ¿Cómo conectar Grafana con Tempo?
### ¿Cómo conectar Grafana con Prometheus?
### ¿Cómo conectar Grafana con Loki?

```yml
grafana:
    image: grafana/grafana:latest
```

