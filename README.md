# Helm chart for simple raw HTTP server

## Install Tiller
While waiting for Helm v3, we will still used Tiller. Let run this command to install Tiller

```
helm init --service-account tiller --override spec.selector.matchLabels.'name'='tiller',spec.selector.matchLabels.'app'='helm' --output yaml | sed 's@apiVersion: extensions/v1beta1@apiVersion: apps/v1@' | kubectl apply -f -
``` 

## Clone the project

```
git clone git@github.com:ezmockup/chart-simple-raw-http-server.git
```

## Install the chart

```
helm install --name your-chart-name ./simple-raw-http-server-chart
```
