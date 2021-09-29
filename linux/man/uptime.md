```
UPTIME(1)                     User Commands                    UPTIME(1)
```

## NAME     [top](https://man7.org/linux/man-pages/man1/uptime.1.html#top_of_page)

```
       uptime - Tell how long the system has been running.
```

## SYNOPSIS     [top](https://man7.org/linux/man-pages/man1/uptime.1.html#top_of_page)

```
       uptime [options]
```

## DESCRIPTION     [top](https://man7.org/linux/man-pages/man1/uptime.1.html#top_of_page)

```
       uptime gives a one line display of the following information.
       The current time, how long the system has been running, how many
       users are currently logged on, and the system load averages for
       the past 1, 5, and 15 minutes.

       This is the same information contained in the header line
       displayed by w(1).

       System load averages is the average number of processes that are
       either in a runnable or uninterruptable state.  A process in a
       runnable state is either using the CPU or waiting to use the CPU.
       A process in uninterruptable state is waiting for some I/O
       access, eg waiting for disk.  The averages are taken over the
       three time intervals.  Load averages are not normalized for the
       number of CPUs in a system, so a load average of 1 means a single
       CPU system is loaded all the time while on a 4 CPU system it
       means it was idle 75% of the time.
```

## OPTIONS     [top](https://man7.org/linux/man-pages/man1/uptime.1.html#top_of_page)

```
       -p, --pretty
              show uptime in pretty format

       -h, --help
              display this help text

       -s, --since
              system up since, in yyyy-mm-dd HH:MM:SS format

       -V, --version
              display version information and exit
```

## FILES     [top](https://man7.org/linux/man-pages/man1/uptime.1.html#top_of_page)

```
       /var/run/utmp
              information about who is currently logged on

       /proc  process information
```

## AUTHORS     [top](https://man7.org/linux/man-pages/man1/uptime.1.html#top_of_page)

```
       uptime was written by Larry Greenfield ⟨greenfie@gauss.rutgers.
       edu⟩ and Michael K. Johnson ⟨johnsonm@sunsite.unc.edu⟩
```

## SEE ALSO     [top](https://man7.org/linux/man-pages/man1/uptime.1.html#top_of_page)

```
       ps(1), top(1), utmp(5), w(1)
```

## REPORTING BUGS     [top](https://man7.org/linux/man-pages/man1/uptime.1.html#top_of_page)

```
       Please send bug reports to ⟨procps@freelists.org⟩
```

## COLOPHON     [top](https://man7.org/linux/man-pages/man1/uptime.1.html#top_of_page)

```
       This page is part of the procps-ng (/proc filesystem utilities)
       project.  Information about the project can be found at 
       ⟨https://gitlab.com/procps-ng/procps⟩.  If you have a bug report
       for this manual page, see
       ⟨https://gitlab.com/procps-ng/procps/blob/master/Documentation/bugs.md⟩.
       This page was obtained from the project's upstream Git repository
       ⟨https://gitlab.com/procps-ng/procps.git⟩ on 2021-08-27.  (At
       that time, the date of the most recent commit that was found in
       the repository was 2021-08-24.)  If you discover any rendering
       problems in this HTML version of the page, or you believe there
       is a better or more up-to-date source for the page, or you have
       corrections or improvements to the information in this COLOPHON
       (which is not part of the original manual page), send a mail to
       man-pages@man7.org

procps-ng                     December 2012                    UPTIME(1)
```