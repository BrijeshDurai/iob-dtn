# iob-dtn
Repository for CSPC32 Internetworking Protocols Project

This is an implementation of IoB-DTN research paper.
For the simplification I have assumed (25 x 25) grid city with some sink stations. The bicycles are assigned stations with uniform distribution and the path of the bicycle is choosen randomly.

Requirenments:

- go 1.13 (http://golang.org)

- python 3.7

- pandas

- matplotlib

- numpy


How to build:

        git clone https://github.com/BrijeshDurai/iob-dtn.git
        
        cd iob-dtn
        
        go mod init iob-dtn

        go build -o iob


How to run:

 ./iob [command line arguments]

        Usage of ./iob:
        
        -buffer-size uint
        
                sensor buffer size (default 20)
        
        -env-time int
                
                simulation time in second (default 30)
        
        -freq uint
                
                number of packets to be generated in a second (default 4)
        
        -num-copies uint
                
                maximum number of copies of a packate in a buffer (default 8)
        
        -num-cycles uint
                
                number of cycles per station (default 8)
                
        -range float
                
                bike sensor range (default 3)
        
        -speed uint
                
                speed of the bicycle, e.g. unit movement in per second (default 1)


e.g. 

        ./iob -buffer-size 40 -num-cycles 10 -num-copies 8 -freq 12


Plot graph:

         python plotLR.py
