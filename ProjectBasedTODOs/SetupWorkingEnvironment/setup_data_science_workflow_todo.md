# NOTES
* when/where/how to use fau cluster
    * jupyter notebook
        * run jupyter notebook on the browser via OnDemand
    * fau cluster terminal 
        * run shell terminal via putty ( I can't really get wsl2 to do x11 portforwarding correctly)

# WAITINGS

 
* summary on what I have trying to solve 2/7/2020
    * about x11 protocol 
        * x11 protocol forwarding with putty. 
            * work perfectly.
            * how fast is it?
        * x11 protocol forwarding with wsl2
            * get 'qt.qpa.xcb: could not connect to display' error
                * https://stackoverflow.com/questions/64092534/opencv-4-4-0-qt-qpa-xcb-could-not-connect-to-display-on-a-remote-ec2-instance
    * ssh forwarding (only tested for jupyter)
        * reference: 
            * https://roamresearch.com/#/app/AdaptiveGraphStucture/page/c8UPAvtvu 
        * every works fine except when connection is trying to establishded, I get the following error
            * note: 
                * I tried connect to koko main node as well as node I reserved using salloc -c 64 -p longq7'
            * 'connection fail' (something like that)

* how to send command to fau cluster from local terminal using ssh?
    * do i get output back to local terminal?
    * if this is possible, the only problem here would be how to view image with x11? 
        * maybe I should try setup plot to update image to s3 when working on remote server terminal such as ec2.
            * https://www.youtube.com/watch?v=qbEn57K7UGw&list=PLdNSZntn0xaU4IAd_vRvbUW_rwcvFxvDe&index=9&ab_channel=xvzf 
        * try using ubuntu gui via wsl2 on window10
            * https://www.youtube.com/watch?v=IL7Jd9rjgrM&ab_channel=DavidBombal
        * try to solve the x11 error when using it in wsl2
            * get 'qt.qpa.xcb: could not connect to display' error
                * https://stackoverflow.com/questions/64092534/opencv-4-4-0-qt-qpa-xcb-could-not-connect-to-display-on-a-remote-ec2-instance

# TODO
* here> what is the data sahape for conv1D?
* set up gpu for data science project 
    * here> can I create docker to run pytorch and tensorflow on Linux and window
        * here> error
            * docker space is full 
                * read the following 
                    * https://aws.amazon.com/blogs/compute/amazon-ecs-and-docker-volume-drivers-amazon-ebs/
            * pip error: dick space is full
        * 
        * how to start docker project 
            * here> git clone my current project to window's equivalent location 
        * here> find container for data-science (that can be easily extensible by me)
            * requirement 
                * user requirement 
                    * I want to send program to be run in docker containers.
                    * devloperment will be done in my laptops
                * system requirement 
                    * everything, program is send to run in docker, no new packages should be 
                        installed, it could just run the program.
                        * ref
                            *
                            https://stackoverflow.com/questions/25305788/how-to-avoid-reinstalling-packages-when-building-docker-image-for-python-project
        * try the following 
            * run docker -> install requirement files 
        * how to install additional packages from the following 
            * https://github.com/anibali/docker-pytorch 
        * create docker in linux that run pytorch 
            * build basic pytorch model. (prebuilt). get it from example .
    * install nvidia-driver for tensorflow-gpu
        * error
            * I have cuda toolkit 11.3, but tensorflow-gpu required 11.0
            * here> tensorflow no moudle found. tensorflow-gpu 
                * here> https://github.com/tensorflow/tensorflow/issues/34318
        * note 
            * check if cudatoolkit is install using 'nvidia-smi'
            * check cuda version using 'nvcc -v'
            * check if cuda can be detected using ( assume that torch works)
                 ```
                    >>> import torch
                    >>> if torch.cuda.is_available():
                    ...   dev = "cuda:0"
                    ... else:
                    ...   dev = "cpu"
                    ...
                    >>> dev
                    'cuda:0'
                    >>> device = torch.device(dev)
                    >>> a = torch.zeros(4,3)
                    >>> a = a.to(device)
                ```
        * here> https://www.tensorflow.org/install/gpu#linux_setup
            * cuda toolkit 11.0
                * https://developer.nvidia.com/cuda-11.0-download-archive?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exenetwork
    * using gpu on window
        * here> install cuda and cudnn
        * figure out how to run gpu in windows.
            * here> how to access wsl folder from outside of wsl?
                * can powershell access folder in wsl? 
                * can I use symbolic link to link to window system and access it?

* get a good understnad of how to launch service directly (unmanaged by an init system).
    * https://unix.stackexchange.com/questions/197437/what-exactly-does-init-do

* setup ec2 autoscaling
    * ref 
        * https://hands-on.cloud/terraform-recipe-managing-auto-scaling-groups-and-load-balancers/
* use Uberzug to view image in vifm.
    * ref: 
        * https://www.youtube.com/watch?v=qgxsduCO1pE&ab_channel=DistroTube
    * figure out workflow for data science

* test using koko3 desktop.
    * asnwer the following (if answer is not satisfy try using virtual machine to get Centos)
        * can I plot in here? using terminal?
        * which key binding works and not work? 
        * does the user experiment okay?

* in koko terminal, I am sure I did 'config checkout' already, but I couldn't find some dotfiles that should be there. such as .tmux .tmux.conf
    * questions:
        * why do i need to use git bare to manage dotfiles in the first place? 
            * read this may help answer the question 
                * https://stegosaurusdormant.com/bare-git-repo/#fnref:no-home-git-repo
            * why can't I just use git repo to manage dotfiles then write a script to move dotfiles
    * figure out a way to do create branches in git bare ( may be i need to create branch first in the git repo then i can do git bare on those branch. (check if this make any sense at all ?))
        * reference:
            https://stackoverflow.com/questions/3301956/git-correct-way-to-change-active-branch-in-a-bare-repository
        * note:
            * this is so taht  i can manage many dotfiles branches 
    * figure out a way for me to debug this.
        * BE CAREFUL, make sure I don't overwrite config that make zsh + vim + tmux work in the koko terminal.
            * is there a way to do git diff?
            * should I wait until I figure out how to use ansible to setup workstation?

* here> watch and implement vim for data science 
    * here> xvzf
        * suckless data science series
            * https://www.youtube.com/watch?v=qbEn57K7UGw&list=PLdNSZntn0xaU4IAd_vRvbUW_rwcvFxvDe&index=9&ab_channel=xvzf 
                * try setup plot to update image to s3 when working on remote server terminal such as ec2.

* fix data science cookie cutter repo on github to be upto date.
* create a github repo for all AI related stuff
    * move /Example and /notebook to this project

    * tutorial + usecase of the following
        * how to build simply network
        * hyperparameter tuning.
* BeyondJupyter
