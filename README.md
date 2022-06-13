![Logo](https://github.com/idealista/prometheus_solr_exporter_role/blob/master/logo.gif)

[![Build Status](https://travis-ci.com/idealista/prometheus_solr_exporter_role.png)](https://travis-ci.com/idealista/prometheus_solr_exporter_role)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-idealista.prometheus_solr_exporter__role-B62682.svg)](https://galaxy.ansible.com/idealista/prometheus_solr_exporter_role)

Solr Prometheus exporter Ansible role
=========

This role installs a Prometheus exporter for Solr

- [Getting Started](#getting-started)
	- [Prerequisites](#prerequisites)
	- [Installing](#installing)
- [Usage](#usage)
- [Testing](#testing)
- [Built With](#built-with)
- [Versioning](#versioning)
- [Authors](#authors)
- [License](#license)
- [Contributing](#contributing)

## Getting started

This role installs a Prometheus exporter for Solr Standalone or Solr Cloud. 
If you need to install Apache Solr use this other role [idealista/solrcloud-role](https://github.com/idealista/solrcloud-role)  

### Prerequesites

Python, Ansible, Molecule and Docker

### Installing

Create or add to your roles dependency file (e.g requirements.yml):

``` yml
- src: idealista.prometheus_solr_exporter_role
  version: 2.0.0
  name: prometheus_solr_exporter
```

Install the role with ansible-galaxy command:

```
ansible-galaxy install -p roles -r requirements.yml -f
```

Use in a playbook:

```
- hosts: someserver
  roles:
    - role: prometheus_solr_exporter
```

## Usage

Variables explanation:

- `prometheus_solr_exporter_version` this is the solr prometheus exporter version to install
- `prometheus_solr_exporter_installation_dir` this is a path location to install the exporter
- `prometheus_solr_exporter_user` user owner of all files
- `prometheus_solr_exporter_group` group owner of all files
- `prometheus_solr_exporter_temp_dir` the path for a temporary directory
- `prometheus_solr_exporter_port` listening port
- `prometheus_solr_exporter_solr_mode` 'standalone' or 'cluster'
- `prometheus_solr_exporter_threads` number of threads
- `prometheus_solr_exporter_config_file` this is the config file path. Use it to override default config file


Excluding variables:

- `prometheus_solr_exporter_zookeeper_host` if cluster mode, the zookeeper host. For ex, http://localhost:8983/solr
- `prometheus_solr_exporter_solr_baseurl` if standalone mode, the solr url. For ex, localhost:2181/solr


## Testing

Run `pip install requirements-test.yml` before running tests

Launch tests:

`molecule test`

## Built With

![Ansible](https://img.shields.io/badge/ansible-5.2.0-green.svg)

## Versioning

For the versions available, see the [tags on this repository](https://github.com/idealista/prometheus_solr_exporter_role/tags).

Additionaly you can see what change in each version in the [CHANGELOG.md](CHANGELOG.md) file.

## Authors

* **Idealista** - *Work with* - [idealista](https://github.com/idealista)

See also the list of [contributors](https://github.com/idealista/prometheus_solr_exporter_role/contributors) who participated in this project.

## License

![Apache 2.0 License](https://img.shields.io/hexpm/l/plug.svg)

This project is licensed under the [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) license - see the [LICENSE](LICENSE) file for details.

## Contributing

Please read [CONTRIBUTING.md](.github/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.
