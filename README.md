# condor_wn

Name:
       condor_wn is a command line tool to gathers information about the HTcondor
       jobs on a cluster and displays it in a pretty format.

Tested:
       Python 2.6 and 2.7

Setup:
       The script should be installed in the directory /usr/local/bin directory
       The condor_wn.yaml file should be located in the /usr/local/etc directory

Synopsis:
       condor_wn  [ --list <all:offline:online:multicore> ] [ --column n ] [ --descending ]
                  [ --summary ]
                  [ --workernode <workernode> ]
                  [ --user <username> ]
                  [ --online <workernode> ]
                  [ --offline <workernode> ]
                  [ --html ]
                  [ --help ]

Description
       condor_wn is a Linux-only tool that displays a snapshot information about jobs running
       on the HTcondor cluster. The condor_wn tool is written in python using the client-side
       APIs for HTCondor and the ClassAd language.
Name
       condor_wn is a command line tool to gathers information about the HTcondor
       jobs on a cluster and displays it in a pretty format.

Tested
       Python 2.6 and 2.7

Setup
       The script should be installed in the directory /usr/local/bin directory
       The condor_wn.yaml file should be located in the /usr/local/etc directory

Synopsis
       condor_wn  [ --list <all:offline:online:multicore> ] [ --column n ] [ --descending ]
                  [ --summary ]
                  [ --workernode <workernode> ]
                  [ --user <username> ]
                  [ --online <workernode> ]
                  [ --offline <workernode> ]
                  [ --html ]
                  [ --help ]

Description
       condor_wn is a Linux-only tool that displays a snapshot information about jobs running
       on the HTcondor cluster. The condor_wn tool is written in python using the client-side
       APIs for HTCondor and the ClassAd language.
Name
       condor_wn is a command line tool to gathers information about the HTcondor
       jobs on a cluster and displays it in a pretty format.

Tested
       Python 2.6 and 2.7

Setup
       The script should be installed in the directory /usr/local/bin directory
       The condor_wn.yaml file should be located in the /usr/local/etc directory

Synopsis
       condor_wn  [ --list <all:offline:online:multicore> ] [ --column n ] [ --descending ]
                  [ --summary ]
                  [ --workernode <workernode> ]
                  [ --user <username> ]
                  [ --online <workernode> ]
                  [ --offline <workernode> ]
                  [ --html ]
                  [ --help ]

Description
       condor_wn is a Linux-only tool that displays a snapshot information about jobs running
       on the HTcondor cluster. The condor_wn tool is written in python using the client-side
       APIs for HTCondor and the ClassAd language.
       html option creates an html file of the above tables

       If multiple worker nodes has to be onlined or offlined, a comma separated list can be used.
       "ALL" input with either --online or --offline option can be used to onlined/offlined all worker nodes.

Options
       --list <all:offline:online:multicore>  {same as -l}
            all:       displays all jobs running on worker nodes
            online:    displays only jobs running on online worker nodes
            offline:   displays only jobs running on offline worker nodes
            multicore: displays only jobs running the more than 1 CPUs on worker nodes

       --column n {same as -c}
            sort the table by column number.

       --descending {same as -d}
            sort the column by descending order.

       --summary {same as -s}
            displays summary tables: Jobs per User, CPU Summary, Jobs Summary
            Additional tables: Held jobs, Idle jobs, Long running jobs and Exceeding CPU
                               threshold jobs if criteria specified in the condor_wn.yaml
                               file is met.

       --workernode <workernode> {same as -w}
            display all jobs running on the worker node. Comma separated list can be used
            to display multiple worker nodes.

       --user <username> {same as -u}
            display all jobs owned by a user running on the worker nodes. Comma separated list can be used
            to display multiple users.

       --online <workernode> {same as -o}
            online worker node. Comma separated list can be used to online worker nodes.

       --offline <workernode> {same as -f}
            offline worker node. Comma separated list can be used to offline worker nodes.

       --html {same as -t}
            create an html file of the tables

       --help {same as -h}
            display simple help
Additional Files
       condor_wn.yaml  Configuration files contains initial settings and html output template.

Exit Status
       condor_wn will exit with a status value of 0 (zero) upon success.

Dependencies
       The following rpms has to be installed to use condor_wn tool:
              condor-classads
              condor-python
              python-prettytable
              PyYAML

Version
       0.21  - 22nd January 2018

Author
       Vipul Davda, Department of Particle Physics, University of Oxford
