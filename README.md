# norc
Norc is a rewrite of cron in bash. Job syntax is compatible with vixie cron.

To run, just execute the script as root. For example:

    nohup ./norc &> /path/to/logfile &

Jobs go into /var/spool/norc. After making changes to the job file, send a SIGHUP to the norc process:
    kill -1 `pidof norc`

Limitations:

It assumes that your job specification has the correct syntax.
