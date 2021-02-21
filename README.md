# jts - Juno's TimeSheet
A little script i made to track my timecard locally in a csv
stores clocks in and out in a csv file, and displays progress in the current pay period

# setup

  Edit the lines in the script after ###SETTINGS### to reflect your setup and work situation

# usage
```
jts [-h] [-i] [-o] [-s] [-d] [-p] [-f TIMESHEET]
            [-D TEST_DATE] [-T TEST_TIME]
arguments:
  -h, --help            show this help message and exit
  -i, --clockIn         add a new punch in
  -o, --clockOut        add a new punch out, report and add hours
                        worked in the session to the file
  -s, --session         display stats about current or last work
                        session
  -d, --day             display stats about current or last
                        workday
  -p, --period          display stats about current pay period
  -f TIMESHEET, --timeSheet TIMESHEET
                        Use specified file instead of the path
                        stored in $TIMESHEET
  -D TEST_DATE, --test_date TEST_DATE
                        use date instead of today for testing
  -T TEST_TIME, --test_time TEST_TIME
                        use date instead of today for testing
```



# alias tip:
in my .zshrc I have the following aliases:
```bash
alias ws='python3 ~/jts -i'
alias we='python3 ~/jts -o'
alias ts='python3 ~/jts -p'
```
This lets me quickly and easily clock in, out, and check my progress
