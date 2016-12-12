# WEBServer

A server that listens for incoming HTTP connection and processes incoming requests. It provides both a WEB UI as well as a REST API in addition to simplifying configuration of WEB Server module.





## Command list

**TODO:** Add a list of all external commands (this is not check commands)

## Configuration list


Common Keys:

| Path / Section | Key | Description|
| -------------- | --- | -----------|
| [/settings/default](#/settings/default) | [allowed hosts](#/settings/default_allowed hosts) | ALLOWED HOSTS|
| [/settings/default](#/settings/default) | [bind to](#/settings/default_bind to) | BIND TO ADDRESS|
| [/settings/default](#/settings/default) | [cache allowed hosts](#/settings/default_cache allowed hosts) | CACHE ALLOWED HOSTS|
| [/settings/default](#/settings/default) | [inbox](#/settings/default_inbox) | INBOX|
| [/settings/default](#/settings/default) | [password](#/settings/default_password) | PASSWORD|
| [/settings/default](#/settings/default) | [timeout](#/settings/default_timeout) | TIMEOUT|
| [/settings/WEB/server](#/settings/WEB/server) | [certificate](#/settings/WEB/server_certificate) | CERTIFICATE|
| [/settings/WEB/server](#/settings/WEB/server) | [port](#/settings/WEB/server_port) | PORT NUMBER|

Advanced keys:

| Path / Section | Key | Description|
| -------------- | --- | -----------|
| [/settings/default](#/settings/default) | [encoding](#/settings/default_encoding) | NRPE PAYLOAD ENCODING|
| [/settings/default](#/settings/default) | [socket queue size](#/settings/default_socket queue size) | LISTEN QUEUE|
| [/settings/default](#/settings/default) | [thread pool](#/settings/default_thread pool) | THREAD POOL|
| [/settings/WEB/server](#/settings/WEB/server) | [allowed hosts](#/settings/WEB/server_allowed hosts) | ALLOWED HOSTS|
| [/settings/WEB/server](#/settings/WEB/server) | [cache allowed hosts](#/settings/WEB/server_cache allowed hosts) | CACHE ALLOWED HOSTS|
| [/settings/WEB/server](#/settings/WEB/server) | [password](#/settings/WEB/server_password) | PASSWORD|






# Configuration



## /settings/default

`/settings/default`






| Key | Default Value | Description|
| --- | ------------- | -----------|
| [allowed hosts](#/settings/default_allowed hosts) | 127.0.0.1 | ALLOWED HOSTS|
| [bind to](#/settings/default_bind to) |  | BIND TO ADDRESS|
| [cache allowed hosts](#/settings/default_cache allowed hosts) | 1 | CACHE ALLOWED HOSTS|
| [encoding](#/settings/default_encoding) |  | NRPE PAYLOAD ENCODING|
| [inbox](#/settings/default_inbox) | inbox | INBOX|
| [password](#/settings/default_password) |  | PASSWORD|
| [socket queue size](#/settings/default_socket queue size) | 0 | LISTEN QUEUE|
| [thread pool](#/settings/default_thread pool) | 10 | THREAD POOL|
| [timeout](#/settings/default_timeout) | 30 | TIMEOUT|


**Sample**::

```
# 
# 
[/settings/default]
allowed hosts=127.0.0.1
bind to=
cache allowed hosts=1
encoding=
inbox=inbox
password=
socket queue size=0
thread pool=10
timeout=30

```


<a name="/settings/default_allowed hosts"/>
### allowed hosts

**ALLOWED HOSTS**

A comaseparated list of allowed hosts. You can use netmasks (/ syntax) or * to create ranges.

**Path**: /settings/default

**Key**: allowed hosts

**Default value**: 127.0.0.1

**Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

**Sample**::

```
[/settings/default]
# ALLOWED HOSTS
allowed hosts=127.0.0.1
```


<a name="/settings/default_bind to"/>
### bind to

**BIND TO ADDRESS**

Allows you to bind server to a specific local address. This has to be a dotted ip address not a host name. Leaving this blank will bind to all available IP addresses.

**Path**: /settings/default

**Key**: bind to

**Default value**: 

**Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

**Sample**::

```
[/settings/default]
# BIND TO ADDRESS
bind to=
```


<a name="/settings/default_cache allowed hosts"/>
### cache allowed hosts

**CACHE ALLOWED HOSTS**

If host names (DNS entries) should be cached, improves speed and security somewhat but won't allow you to have dynamic IPs for your Nagios server.

**Path**: /settings/default

**Key**: cache allowed hosts

**Default value**: 1

**Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

**Sample**::

```
[/settings/default]
# CACHE ALLOWED HOSTS
cache allowed hosts=1
```


<a name="/settings/default_encoding"/>
### encoding

**NRPE PAYLOAD ENCODING**



**Advanced** (means it is not commonly used)

**Path**: /settings/default

**Key**: encoding

**Default value**: 

**Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

**Sample**::

```
[/settings/default]
# NRPE PAYLOAD ENCODING
encoding=
```


<a name="/settings/default_inbox"/>
### inbox

**INBOX**

The default channel to post incoming messages on

**Path**: /settings/default

**Key**: inbox

**Default value**: inbox

**Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

**Sample**::

```
[/settings/default]
# INBOX
inbox=inbox
```


<a name="/settings/default_password"/>
### password

**PASSWORD**

Password used to authenticate against server

**Path**: /settings/default

**Key**: password

**Default value**: 

**Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

**Sample**::

```
[/settings/default]
# PASSWORD
password=
```


<a name="/settings/default_socket queue size"/>
### socket queue size

**LISTEN QUEUE**

Number of sockets to queue before starting to refuse new incoming connections. This can be used to tweak the amount of simultaneous sockets that the server accepts.

**Advanced** (means it is not commonly used)

**Path**: /settings/default

**Key**: socket queue size

**Default value**: 0

**Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

**Sample**::

```
[/settings/default]
# LISTEN QUEUE
socket queue size=0
```


<a name="/settings/default_thread pool"/>
### thread pool

**THREAD POOL**



**Advanced** (means it is not commonly used)

**Path**: /settings/default

**Key**: thread pool

**Default value**: 10

**Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

**Sample**::

```
[/settings/default]
# THREAD POOL
thread pool=10
```


<a name="/settings/default_timeout"/>
### timeout

**TIMEOUT**

Timeout when reading packets on incoming sockets. If the data has not arrived within this time we will bail out.

**Path**: /settings/default

**Key**: timeout

**Default value**: 30

**Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

**Sample**::

```
[/settings/default]
# TIMEOUT
timeout=30
```




## /settings/WEB/server

`/settings/WEB/server`

**WEB SERVER SECTION**

Section for WEB (WEBServer.dll) (check_WEB) protocol options.


| Key | Default Value | Description|
| --- | ------------- | -----------|
| [allowed hosts](#/settings/WEB/server_allowed hosts) | 127.0.0.1 | ALLOWED HOSTS|
| [cache allowed hosts](#/settings/WEB/server_cache allowed hosts) | 1 | CACHE ALLOWED HOSTS|
| [certificate](#/settings/WEB/server_certificate) | ${certificate-path}/certificate.pem | CERTIFICATE|
| [password](#/settings/WEB/server_password) |  | PASSWORD|
| [port](#/settings/WEB/server_port) | 8443s | PORT NUMBER|


**Sample**::

```
# WEB SERVER SECTION
# Section for WEB (WEBServer.dll) (check_WEB) protocol options.
[/settings/WEB/server]
allowed hosts=127.0.0.1
cache allowed hosts=1
certificate=${certificate-path}/certificate.pem
password=
port=8443s

```


<a name="/settings/WEB/server_allowed hosts"/>
### allowed hosts

**ALLOWED HOSTS**

A comaseparated list of allowed hosts. You can use netmasks (/ syntax) or * to create ranges. parent for this key is found under: /settings/default this is marked as advanced in favor of the parent.

**Advanced** (means it is not commonly used)

**Path**: /settings/WEB/server

**Key**: allowed hosts

**Default value**: 127.0.0.1

**Used by**: :module:`WEBServer`

**Sample**::

```
[/settings/WEB/server]
# ALLOWED HOSTS
allowed hosts=127.0.0.1
```


<a name="/settings/WEB/server_cache allowed hosts"/>
### cache allowed hosts

**CACHE ALLOWED HOSTS**

If host names (DNS entries) should be cached, improves speed and security somewhat but won't allow you to have dynamic IPs for your Nagios server. parent for this key is found under: /settings/default this is marked as advanced in favor of the parent.

**Advanced** (means it is not commonly used)

**Path**: /settings/WEB/server

**Key**: cache allowed hosts

**Default value**: 1

**Used by**: :module:`WEBServer`

**Sample**::

```
[/settings/WEB/server]
# CACHE ALLOWED HOSTS
cache allowed hosts=1
```


<a name="/settings/WEB/server_certificate"/>
### certificate

**CERTIFICATE**

Ssl certificate to use for the ssl server

**Path**: /settings/WEB/server

**Key**: certificate

**Default value**: ${certificate-path}/certificate.pem

**Used by**: :module:`WEBServer`

**Sample**::

```
[/settings/WEB/server]
# CERTIFICATE
certificate=${certificate-path}/certificate.pem
```


<a name="/settings/WEB/server_password"/>
### password

**PASSWORD**

Password used to authenticate against server parent for this key is found under: /settings/default this is marked as advanced in favor of the parent.

**Advanced** (means it is not commonly used)

**Path**: /settings/WEB/server

**Key**: password

**Default value**: 

**Used by**: :module:`WEBServer`

**Sample**::

```
[/settings/WEB/server]
# PASSWORD
password=
```


<a name="/settings/WEB/server_port"/>
### port

**PORT NUMBER**

Port to use for WEB server.

**Path**: /settings/WEB/server

**Key**: port

**Default value**: 8443s

**Used by**: :module:`WEBServer`

**Sample**::

```
[/settings/WEB/server]
# PORT NUMBER
port=8443s
```

