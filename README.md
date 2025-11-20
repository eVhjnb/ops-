## CRON jobs on Ubuntu

This project is scheduled on an Ubuntu server using `crontab` and one virtualenv per job folder under `/var/cjobs`.

Pattern used:

- `/var/cjobs/success-scorecard`
- `/var/cjobs/leadership-scorecard`
- `/var/cjobs/applications-scorecard`
- `/var/cjobs/inside-jobs`

Each folder contains:

- a dedicated Python virtualenv (`venv/`)
- one or more Python entrypoints (`run_*_scorecard.py`, maintenance scripts)
- local log files (e.g. `cronjob.log`, `exportar_logs_csv.log`)

CRON runs:

- weekly scorecard generation (Success, Leadership, Applications)
- monthly maintenance jobs (log export and cleanup)
