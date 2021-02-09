#RESOURCES
* introduction to parrallel programming with MPI and Python
    * https://www.youtube.com/watch?v=36nCgG40DJo&ab_channel=SharcnetHPC
    * mpi for deep learning 
        * https://www.youtube.com/results?search_query=mpi+for+deep+learning&page&utm_source=opensearch
        * https://www.youtube.com/watch?v=onwBKVFdXzc&ab_channel=PyOhio
        * https://www.youtube.com/watch?v=FrJM2dH57jo&ab_channel=PyOhio
* supercomputing/HPC with python
    * https://www.youtube.com/watch?v=3F7P2lAD6hw&ab_channel=sentdex
* multiprocessing in Python
    * https://www.youtube.com/watch?v=RR4SoktDQAw&ab_channel=LucidProgramming

* Estimating CPU performance using Amdahls Law
    * https://www.pugetsystems.com/labs/articles/Estimating-CPU-Performance-using-Amdahls-Law-619/

* Optimize your CPU for Deep Learning
    * https://towardsdatascience.com/optimize-your-cpu-for-deep-learning-424a199d7a87


#NOTE
* read Running Graphical Application
    * https://wiki.ubuntu.com/WSL#Running_Graphical_Applications 
        * what is x window system architecture?
            * https://wiki.ubuntu.com/X/Architecture
    * what is X Window System Architec?
        * X server 
            * can be native window server givne OpenGL
        * X client
            * client can be graphical linux application  running in WSL environment


#QUESTION

#WAITING

#OPTIMIZATION

#TODO

* here> learn how to use slurm job management
    * here> https://hpc.fau.edu/interactive-and-gui-based-jobs/
        * here> Goal: running graphic (such as matplotlib using X11 on wsl once work make it run on FAU cluster(or other grpahcial protocol)
            * here> how to setup x11 in WSL2 ( try putty if too time comsuming; allow for copy and paste by mouse)
                * here> x11 in Ubuntu
                    * here> try plotting graph in fau host computer. 
                        * here> without ssh and with ssh 
                            * solution
                                * sol1: remote window access to wsl (ubuntu) all within my window 10
                                    * ref
                                        * https://www.youtube.com/watch?v=IL7Jd9rjgrM&ab_channel=DavidBombal
                                * sol2: wsl2 gui with xserver
                                    * ref
                                        * https://www.youtube.com/watch?v=uL8nnuvybL8&ab_channel=TheRealNetworkLab 
                            * Error: 
                                * error when run program to plot with  matplotlib
                                    * No DISPLAY variable set, cannot setup x11 forwarding. 
                                        * https://unix.stackexchange.com/questions/12755/how-to-forward-x-over-ssh-to-run-graphics-applications-remotely
    * try running the following:
        * https://hpc.fau.edu/engineering-queue-gpus/
            * the article show implementation of GPU and slurm (via sbatch)
                lets run something that would require cluter and compare speed. 
        * use metrics show in this video to measure speed
            * https://www.youtube.com/watch?v=4lKcou1-3OY&ab_channel=PyConAU at 18.49
        * how to test cluster vs non cluster speed ( this is needed to validate that cluster is being used)
        * how to test GPU vs CPU speed.
        * when using cluster does it run with CPU or GPU?
            * is this part of the configurtion that I have to set?


* Goal: learning all the ways to write faster code (focus on Deep learning code)
    * learning gpu programming (practical: looking for code in github)
        * note
            * only allow for learning by working on code myself
        * learn Numba
            * reference:
                * https://developer.nvidia.com/how-to-cuda-python 
                    * getting started with GPU 
                * https://github.com/carl9384/cuda

    * learn high performance computing Theory (course like leanring environment)
        *  reference:    
            course
            https://www.udacity.com/course/high-performance-computer-architecture--ud007


