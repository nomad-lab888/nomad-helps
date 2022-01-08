# nomad monitor -help

Usage: nomad monitor [options]

Stream log messages of a nomad agent. The monitor command lets you
listen for log levels that may be filtered out of the Nomad agent. For
example your agent may only be logging at INFO level, but with the monitor
command you can set -log-level DEBUG

When ACLs are enabled, this command requires a token with the 'agent:read'
capability.

General Options:

-address=<addr>
The address of the Nomad server.
Overrides the NOMAD_ADDR environment variable if set.
Default = http://127.0.0.1:4646

-region=<region>
The region of the Nomad servers to forward commands to.
Overrides the NOMAD_REGION environment variable if set.
Defaults to the Agent's local region.

-no-color
Disables colored command output. Alternatively, NOMAD_CLI_NO_COLOR may be
set. This option takes precedence over -force-color.

-force-color
Forces colored command output. This can be used in cases where the usual
terminal detection fails. Alternatively, NOMAD_CLI_FORCE_COLOR may be set.
This option has no effect if -no-color is also used.

-ca-cert=<path>
Path to a PEM encoded CA cert file to use to verify the
Nomad server SSL certificate. Overrides the NOMAD_CACERT
environment variable if set.

-ca-path=<path>
Path to a directory of PEM encoded CA cert files to verify
the Nomad server SSL certificate. If both -ca-cert and
-ca-path are specified, -ca-cert is used. Overrides the
NOMAD_CAPATH environment variable if set.

-client-cert=<path>
Path to a PEM encoded client certificate for TLS authentication
to the Nomad server. Must also specify -client-key. Overrides
the NOMAD_CLIENT_CERT environment variable if set.

-client-key=<path>
Path to an unencrypted PEM encoded private key matching the
client certificate from -client-cert. Overrides the
NOMAD_CLIENT_KEY environment variable if set.

-tls-server-name=<value>
The server name to use as the SNI host when connecting via
TLS. Overrides the NOMAD_TLS_SERVER_NAME environment variable if set.

-tls-skip-verify
Do not verify TLS certificate. This is highly not recommended. Verification
will also be skipped if NOMAD_SKIP_VERIFY is set.

-token
The SecretID of an ACL token to use to authenticate API requests with.
Overrides the NOMAD_TOKEN environment variable if set.

Monitor Specific Options:

-log-level <level>
Sets the log level to monitor (default: INFO)

-node-id <node-id>
Sets the specific node to monitor

-server-id <server-id>
Sets the specific server to monitor

-json
Sets log output to JSON format
root@dev1:~# nomad monitor -help
Usage: nomad monitor [options]

Stream log messages of a nomad agent. The monitor command lets you
listen for log levels that may be filtered out of the Nomad agent. For
example your agent may only be logging at INFO level, but with the monitor
command you can set -log-level DEBUG

When ACLs are enabled, this command requires a token with the 'agent:read'
capability.

General Options:

-address=<addr>
The address of the Nomad server.
Overrides the NOMAD_ADDR environment variable if set.
Default = http://127.0.0.1:4646

-region=<region>
The region of the Nomad servers to forward commands to.
Overrides the NOMAD_REGION environment variable if set.
Defaults to the Agent's local region.

-no-color
Disables colored command output. Alternatively, NOMAD_CLI_NO_COLOR may be
set. This option takes precedence over -force-color.

-force-color
Forces colored command output. This can be used in cases where the usual
terminal detection fails. Alternatively, NOMAD_CLI_FORCE_COLOR may be set.
This option has no effect if -no-color is also used.

-ca-cert=<path>
Path to a PEM encoded CA cert file to use to verify the
Nomad server SSL certificate. Overrides the NOMAD_CACERT
environment variable if set.

-ca-path=<path>
Path to a directory of PEM encoded CA cert files to verify
the Nomad server SSL certificate. If both -ca-cert and
-ca-path are specified, -ca-cert is used. Overrides the
NOMAD_CAPATH environment variable if set.

-client-cert=<path>
Path to a PEM encoded client certificate for TLS authentication
to the Nomad server. Must also specify -client-key. Overrides
the NOMAD_CLIENT_CERT environment variable if set.

-client-key=<path>
Path to an unencrypted PEM encoded private key matching the
client certificate from -client-cert. Overrides the
NOMAD_CLIENT_KEY environment variable if set.

-tls-server-name=<value>
The server name to use as the SNI host when connecting via
TLS. Overrides the NOMAD_TLS_SERVER_NAME environment variable if set.

-tls-skip-verify
Do not verify TLS certificate. This is highly not recommended. Verification
will also be skipped if NOMAD_SKIP_VERIFY is set.

-token
The SecretID of an ACL token to use to authenticate API requests with.
Overrides the NOMAD_TOKEN environment variable if set.

Monitor Specific Options:

-log-level <level>
Sets the log level to monitor (default: INFO)

-node-id <node-id>
Sets the specific node to monitor

-server-id <server-id>
Sets the specific server to monitor

-json
Sets log output to JSON format