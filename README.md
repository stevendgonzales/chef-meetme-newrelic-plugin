meetme-newrelic-plugin Cookbook
===============================
Installs the MeetMe plugin for NewRelic


Requirements
------------
python
python-pip
newrelic


Attributes
----------
#### meetme-newrelic-plugin::default
* `node[:meetme_newrelic_plugin][:package_name]` - The name of the pip package that installs the meetme newrelic plugin  
* `node[:meetme_newrelic_plugin][:poll_interval]` - interval, in seconds, that stats are polled  
* `node[:meetme_newrelic_plugin][:config_file]` -  location of config file
* `node[:meetme_newrelic_plugin][:log_dir]` - logging directory
* `node[:meetme_newrelic_plugin][:log_file]` - name of log file
* `node[:meetme_newrelic_plugin][:run_dir]` -  the run directory for the pid file
* `node[:meetme_newrelic_plugin][:user]` -  the user that runs the application 
* `node[:meetme_newrelic_plugin][:group]` -  group for application file permissions 

#### meetme-newrelic-plugin::elasticsearch
* `node[:meetme_newrelic_plugin][:elasticsearch][:clustername]` - name of es cluster
* `node[:meetme_newrelic_plugin][:elasticsearch][:host]` - hostname for es node to monitor
* `node[:meetme_newrelic_plugin][:elasticsearch][:port]` - port es is listening on
* `node[:meetme_newrelic_plugin][:elasticsearch][:scheme]` - http (protocol for connection)


#### meetme-newrelic-plugin::memcached
* `node[:meetme_newrelic_plugin][:memcached][:name]` - hostname memcached instance is running on
* `node[:meetme_newrelic_plugin][:memcached][:host]` - host memcached instance is running on
* `node[:meetme_newrelic_plugin][:memcached][:port]` - port memcached is listening on
* `node[:meetme_newrelic_plugin][:memcached][:path]` - path of unix socket (if memcached is using one)

#### meetme-newrelic-plugin::mongodb
* `node[:meetme_newrelic_plugin][:mongodb][:host]` - host mongodb instance is running on
* `node[:meetme_newrelic_plugin][:mongodb][:port]` - port mongdb is listening on
* `node[:meetme_newrelic_plugin][:mongodb][:database]` - name of database to monitor
* `node[:meetme_newrelic_plugin][:mongodb][:databag_name]` - name of databag that holds mongo config
* `node[:meetme_newrelic_plugin][:mongodb][:databag_item_name]` - name of databag item for mongo config
* `node[:meetme_newrelic_plugin][:mongodb][:admin_username_key]` - key for admin username
* `node[:meetme_newrelic_plugin][:mongodb][:admin_password_key]` - key for admin password
* `node[:meetme_newrelic_plugin][:mongodb][:db_username_key]` - key for db username
* `node[:meetme_newrelic_plugin][:mongodb][:db_password_key]` - key for db password

#### meetme-newrelic-plugin::nginx
* `node[:meetme_newrelic_plugin][:nginx][:name]` - hostname nginx is running on
* `node[:meetme_newrelic_plugin][:nginx][:host]` - host nginx is listening on
* `node[:meetme_newrelic_plugin][:nginx][:port]` - port nginx is listening on
* `node[:meetme_newrelic_plugin][:nginx][:path]` - path of nginx stub status page
* `node[:meetme_newrelic_plugin][:nginx][:verify_ssl_cert]` - verify ssl certificate flag

#### meetme-newrelic-plugin::php_fpm
* `node[:meetme_newrelic_plugin][:php_fpm][:name]` - hostname php-fpm is running on
* `node[:meetme_newrelic_plugin][:php_fpm][:scheme]` - fpm scheme (ex: http or https)
* `node[:meetme_newrelic_plugin][:php_fpm][:host]` - host where fpm status page is listening
* `node[:meetme_newrelic_plugin][:php_fpm][:port]` - port where fpm status page is listening
* `node[:meetme_newrelic_plugin][:php_fpm][:path]` - path of fpm status page 
* `node[:meetme_newrelic_plugin][:php_fpm][:query]` - query type (ex: json)

#### meetme-newrelic-plugin::postgresql
* `node[:meetme_newrelic_plugin][:postgresql][:host]` - host address where postgresql is running
* `node[:meetme_newrelic_plugin][:postgresql][:port]` - port postgresql is listening
* `node[:meetme_newrelic_plugin][:postgresql][:user]` - postgresql user
* `node[:meetme_newrelic_plugin][:postgresql][:dbname]` - db to monitor
* `node[:meetme_newrelic_plugin][:postgresql][:password]` - postgresql password
* `node[:meetme_newrelic_plugin][:postgresql][:superuser]` - hostname uwsgi is running on
* `node[:meetme_newrelic_plugin][:postgresql][:psycopg2_install_method]` - pip || package - install method for postgresql client driver 

#### meetme-newrelic-plugin::uwsgi
* `node[:meetme_newrelic_plugin][:uwsgi][:name]` - hostname uwsgi is running on
* `node[:meetme_newrelic_plugin][:uwsgi][:host]` - host address uwsgi is runnin on
* `node[:meetme_newrelic_plugin][:uwsgi][:port]` - port uwsgi is running on
* `node[:meetme_newrelic_plugin][:uwsgi][:path]` - '/path/to/unix/socket' only set if using unix socket over host:port

Usage
-----
Just include `meetme-newrelic-plugin` in your node's `run_list`:

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[meetme-newrelic-plugin]"
  ]
}
```

Contributing
------------
1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write you change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request using Github

License and Authors
-------------------
Authors: Steven Gonzales
