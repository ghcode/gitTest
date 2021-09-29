```
FREE(1)                       User Commands                      FREE(1)
```

## NAME     [top](https://man7.org/linux/man-pages/man1/free.1.html#top_of_page)

```
       free - Display amount of free and used memory in the system
```

## SYNOPSIS     [top](https://man7.org/linux/man-pages/man1/free.1.html#top_of_page)

```
       free [options]
```

## DESCRIPTION     [top](https://man7.org/linux/man-pages/man1/free.1.html#top_of_page)

```
       free displays the total amount of free and used physical and swap
       memory in the system, as well as the buffers and caches used by
       the kernel. The information is gathered by parsing /proc/meminfo.
       The displayed columns are:

       total  Total installed memory (MemTotal and SwapTotal in
              /proc/meminfo)

       used   Used memory (calculated as total - free - buffers - cache)

       free   Unused memory (MemFree and SwapFree in /proc/meminfo)

       shared Memory used (mostly) by tmpfs (Shmem in /proc/meminfo)

       buffers
              Memory used by kernel buffers (Buffers in /proc/meminfo)

       cache  Memory used by the page cache and slabs (Cached and
              SReclaimable in /proc/meminfo)

       buff/cache
              Sum of buffers and cache

       available
              Estimation of how much memory is available for starting
              new applications, without swapping. Unlike the data
              provided by the cache or free fields, this field takes
              into account page cache and also that not all reclaimable
              memory slabs will be reclaimed due to items being in use
              (MemAvailable in /proc/meminfo, available on kernels 3.14,
              emulated on kernels 2.6.27+, otherwise the same as free)
```

## OPTIONS     [top](https://man7.org/linux/man-pages/man1/free.1.html#top_of_page)

```
       -b, --bytes
              Display the amount of memory in bytes.

       -k, --kibi
              Display the amount of memory in kibibytes.  This is the
              default.

       -m, --mebi
              Display the amount of memory in mebibytes.

       -g, --gibi
              Display the amount of memory in gibibytes.

       --tebi Display the amount of memory in tebibytes.

       --pebi Display the amount of memory in pebibytes.

       --kilo Display the amount of memory in kilobytes. Implies --si.

       --mega Display the amount of memory in megabytes. Implies --si.

       --giga Display the amount of memory in gigabytes. Implies --si.

       --tera Display the amount of memory in terabytes. Implies --si.

       --peta Display the amount of memory in petabytes. Implies --si.

       -h, --human
              Show all output fields automatically scaled to shortest
              three digit unit and display the units of print out.
              Following units are used.

                B = bytes
                Ki = kibibyte
                Mi = mebibyte
                Gi = gibibyte
                Ti = tebibyte
                Pi = pebibyte

              If unit is missing, and you have exbibyte of RAM or swap,
              the number is in tebibytes and columns might not be
              aligned with header.

       -w, --wide
              Switch to the wide mode. The wide mode produces lines
              longer than 80 characters. In this mode buffers and cache
              are reported in two separate columns.

       -c, --count count
              Display the result count times.  Requires the -s option.

       -l, --lohi
              Show detailed low and high memory statistics.

       -s, --seconds delay
              Continuously display the result delay  seconds apart.  You
              may actually specify any floating point number for delay
              using either . or , for decimal point.  usleep(3) is used
              for microsecond resolution delay times.

       --si   Use kilo, mega, giga etc (power of 1000) instead of kibi,
              mebi, gibi (power of 1024).

       -t, --total
              Display a line showing the column totals.

       --help Print help.

       -V, --version
              Display version information.
```

## FILES     [top](https://man7.org/linux/man-pages/man1/free.1.html#top_of_page)

```
       /proc/meminfo
              memory information
```

## BUGS     [top](https://man7.org/linux/man-pages/man1/free.1.html#top_of_page)

```
       The value for the shared column is not available from kernels
       before 2.6.32 and is displayed as zero.

       Please send bug reports to
              ⟨procps@freelists.org⟩
```

## SEE ALSO     [top](https://man7.org/linux/man-pages/man1/free.1.html#top_of_page)

```
       ps(1), slabtop(1), top(1), vmstat(8).
```

## COLOPHON     [top](https://man7.org/linux/man-pages/man1/free.1.html#top_of_page)

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

procps-ng                      2018-05-31                        FREE(1)
```