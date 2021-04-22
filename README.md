# Timecard
A simple CLI utility for keeping track of allocations

# Installation
Requires `gawk`

```
# install gawk on ubuntu 
sudo apt-get install gawk

# install gawk on mac
brew install gawk
```

Set default text editor for manually chaning allocations file

```
echo export EDITOR="vim" >> ~/.bashrc
```

Clone repo and copy `timecard` to path folder

```
cp timecard /usr/local/bin
```

Add alias to `.bashrc`

```
echo alias t="timecard" >> ~/.bashrc`
```

# Usage

```
# add 15 hour allocation to gsa project
t gsa 15

# log 0.75 hours to gsa project
t gsa -0.75

# generate report
t -r

# manually edit timecard
t -e
```

# Example Report

```
ALLOCATIONS:

    Project            Total    Used    Remain
    ---------------    -----    ----    ------
    mothr.mobility     20       6.5     13.5  
    unmccc             15       1       14    
    admin              0        1.75    -1.75 
    prac               0        0.75    -0.75 
    steelnet           5        0       5     
    meduit             20       14      6     
    gsa                15       0       15    

TOTALS:

    Date     Hrs  
    -----    -----
    04/19    -8   
    04/20    -8   
    04/21    -8   

LOG:

    Date     Project            Hrs  
    -----    ---------------    -----
    04/19    admin              1    
    04/19    meduit             7    
    04/20    meduit             7    
    04/20    unmccc             1    
    04/21    admin              0.75 
    04/21    mothr.mobility     6.5  
    04/21    prac               0.75 
```
