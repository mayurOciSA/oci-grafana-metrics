# About OCI Metrics for Grafana

## Installation

### Oracle Cloud Infrastructure Metrics Data Source

## Introduction

This plugin makes queries to the Oracle Cloud Infrastructure Monitoring 
Service and displays them on Grafana.

If you are running Grafana on a machine instance in Oracle Cloud, use the 
Service Principal with a configured Dynamic Group and policy to allow you to 
read metrics and compartments.

If you are running Grafana anywhere else, make sure you have `~/.oci` 
configured properly. You can do this by installing the Oracle Cloud CLI and 
running the setup.

## Note

You need Grafana 8.x.x version installed for OCI Metrics for Grafana installation

In order to simplify the installation process, we created detailed guides for you to follow:

* Install Grafana and the OCI Metrics for Grafana
 on a Linux host using [this document](https://github.com/oracle/oci-grafana-plugin/blob/master/docs/linux.md).
* Install Grafana and the OCI Metrics for Grafana
 on a MacOS host using [this document](https://github.com/oracle/oci-grafana-plugin/blob/master/docs/macos.md).
* Install Grafana and the OCI Metrics for Grafana
 on a virtual machine in Oracle Cloud Infrastructure using [this document](https://github.com/oracle/oci-grafana-plugin/blob/master/docs/linuxoci.md).
* Install Grafana and OCI Metrics for Grafana
on a virtual machine in Oracle Cloud Infrastructure using Terraform using [this document](https://github.com/oracle/oci-grafana-plugin/blob/master/docs/terraform.md).
* Install Grafana and the OCI Metrics for Grafana
on Kubernetes in Oracle Cloud Infrastructure using [this document](https://github.com/oracle/oci-grafana-plugin/blob/master/docs/kubernetes.md)

Once you have the OCI Metrics for Grafana installed, configure your datasource with your 
tenancy OCID, default region, and where you're running the plugin 
(Oracle Cloud or elsewhere).

We also have documentation for how to use the newly installed and configured 
plugin in our [Using Grafana with Oracle Cloud Infrastructure Data Source](https://github.com/oracle/oci-grafana-plugin/blob/master/docs/using.md) walkthrough.

### Debugging

Please make sure that the golang version installed is ```1.16``` and grafana version installed is 8.x.x 

If you want to debug golang backend plugin code, follow the steps below:

* Install [gops](https://github.com/google/gops) to list running go processes on your machine
* Run `gops` and find processId for `oci-plugin_darwin_amd64` process
* Copy this processId to the `.vscode/launch.json`
* In your VSCode from 'Debug' menu call 'Start Debugging'

## Documentation

Please refer to the [docs folder in this repo](./docs)

## Help

Issues and questions about this plugin can be posted [as an issue in this GitHub repository](https://github.com/oracle/oci-grafana-plugin/issues)

## Contributing

This project welcomes contributions from the community. Before submitting a pull
request, please [review our contribution guide](./CONTRIBUTING.md).

## Security

Please consult the [security guide](./SECURITY.md) for our responsible security
vulnerability disclosure process.

## License

Copyright (c) 2021 Oracle and/or its affiliates.

Released under the Universal Permissive License v1.0 as shown at
<https://oss.oracle.com/licenses/upl/>.
