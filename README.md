# pm2-graylog

pm2 module for logging to Graylog.

Inspired by [pm2-gelf-pro](https://github.com/sethblack/pm2-gelf-pro)

## Features

- Support JSON format
- Support [pino.js](https://github.com/pinojs/pino) logs
- Log levels mapping

## Installation

```sh
pm2 install pm2-gelf-json
```

## Needs

When set `pm2 set pm2-gelf-json:pm2LogType 'json'`, needs:

ecosystem.config.js of PM2: `log_type: 'json'`

## Configuration

```sh
$> pm2 set pm2-gelf-json:graylogHost graylog.myserver.org
$> pm2 set pm2-gelf-json:graylogPort 12201
$> pm2 set pm2-gelf-json:graylogLogParseErrors true
$> pm2 set pm2-gelf-json:graylogSplitLines true
$> pm2 set pm2-gelf-json:gelfCustomConfigs '{"optionKey": "optionValue"}'
$> pm2 set pm2-gelf-json:gelfAdapterName 'udp'
$> pm2 set pm2-gelf-json:gelfLogLevelsMapping '0:7,10:7,20:7,30:6,40:4,50:3,60:0'
# default normal string
# pm2 set pm2-gelf-json:pm2LogType 'json'
# pm2 set pm2-gelf-json:graylogType 'json'
```
