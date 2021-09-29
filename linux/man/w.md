```
W(1)                          User Commands                         W(1)
```

## NAME     [top](https://man7.org/linux/man-pages/man1/w.1.html#top_of_page)

```
       w - Show who is logged on and what they are doing.
```

## SYNOPSIS     [top](https://man7.org/linux/man-pages/man1/w.1.html#top_of_page)

```
       w [options] user [...]
```

## DESCRIPTION     [top](https://man7.org/linux/man-pages/man1/w.1.html#top_of_page)

```
       w displays information about the users currently on the machine,
       and their processes.  The header shows, in this order, the
       current time, how long the system has been running, how many
       users are currently logged on, and the system load averages for
       the past 1, 5, and 15 minutes.

       The following entries are displayed for each user: login name,
       the tty name, the remote host, login time, idle time, JCPU, PCPU,
       and the command line of their current process.

       The JCPU time is the time used by all processes attached to the
       tty.  It does not include past background jobs, but does include
       currently running background jobs.

       The PCPU time is the time used by the current process, named in
       the "what" field.
```

## COMMAND-LINE OPTIONS     [top](https://man7.org/linux/man-pages/man1/w.1.html#top_of_page)

```
       -h, --no-header
              Don't print the header.

       -u, --no-current
              Ignores the username while figuring out the current
              process and cpu times.  To demonstrate this, do a su and
              do a w and a w -u.

       -s, --short
              Use the short format.  Don't print the login time, JCPU or
              PCPU times.

       -f, --from
              Toggle printing the from (remote hostname) field.  The
              default as released is for the from field to not be
              printed, although your system administrator or
              distribution maintainer may have compiled a version in
              which the from field is shown by default.

       --help Display help text and exit.

       -i, --ip-addr
              Display IP address instead of hostname for from field.

       -V, --version
              Display version information.

       -o, --old-style
              Old style output.  Prints blank space for idle times less
              than one minute.

       user   Show information about the specified user only.
```

## ENVIRONMENT     [top](https://man7.org/linux/man-pages/man1/w.1.html#top_of_page)

```
       PROCPS_USERLEN
              Override the default width of the username column.
              Defaults to 8.

       PROCPS_FROMLEN
              Override the default width of the from column.  Defaults
              to 16.
```

## FILES     [top](https://man7.org/linux/man-pages/man1/w.1.html#top_of_page)

```
       /var/run/utmp
              information about who is currently logged on

       /proc  process information
```

## SEE ALSO     [top](https://man7.org/linux/man-pages/man1/w.1.html#top_of_page)

```
       free(1), ps(1), top(1), uptime(1), utmp(5), who(1)
```

## AUTHORS     [top](https://man7.org/linux/man-pages/man1/w.1.html#top_of_page)

```
       w was re-written almost entirely by Charles Blake, based on the
       version by Larry Greenfield ⟨greenfie@gauss.rutgers.edu⟩ and
       Michael K. Johnson ⟨johnsonm@redhat.com⟩
```

## REPORTING BUGS     [top](https://man7.org/linux/man-pages/man1/w.1.html#top_of_page)

```
       Please send bug reports to ⟨procps@freelists.org⟩
```

## COLOPHON     [top](https://man7.org/linux/man-pages/man1/w.1.html#top_of_page)

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

procps-ng                      2020-06-04                           W(1)
```