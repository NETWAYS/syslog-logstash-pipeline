# syslog-logstash-pipeline

[![CI](https://github.com/NETWAYS/syslog-logstash-pipeline/workflows/Logstash%20Syntax/badge.svg?event=push)](https://github.com/NETWAYS/syslog-logstash-pipeline/actions?query=workflow%3A%22Logstash+Syntax%22)

Logstash pipeline for basic syslog lines

## Inputs and Outputs ##

If you use files called `input.conf` and `output.conf` they will not collide with this rules, even when you want to pull new versions.

### Examples ###

Here's an example for an `input.conf`

```
input {
  redis {
    host => "localhost"
    data_type => "list"
    key => "netways-syslog-input"
  }
}
```

and one for `output.conf`.

```
output {
  redis {
    host => "localhost"
    data_type => "list"
    key => "netways-syslog-output"
  }
}
```
