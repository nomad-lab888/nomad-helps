# nomad eval -help

Usage: nomad eval <subcommand> [options] [args]

This command groups subcommands for interacting with evaluations. Evaluations
are used to trigger a scheduling event. As such, evaluations are an internal
detail but can be useful for debugging placement failures when the cluster
does not have the resources to run a given job.

Examine an evaluations status:

      $ nomad eval status <eval-id>

Please see the individual subcommand help for detailed usage information.

Subcommands:  
status Display evaluation status and placement failure reasons
