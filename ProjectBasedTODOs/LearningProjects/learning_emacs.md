# NOTE

* once I am sufficient enough with emacs I can try learning emacs using doom emacs. 
    * note 
        * there are so much stuff in doom emacs. it is difficult to know which error cause by emacs and which error caused by the additional layers)


# Reference 

* Threads 
    * advice on how to learns source code in emacs 
        * https://www.reddit.com/r/emacs/comments/7i2alo/how_to_read_and_understand_gnu_emacs_source_code/ 

* Tutorial 
    - eshell tutorial
        - https://www.youtube.com/watch?v=RhYNu6i_uY4&ab_channel=HowardAbramsHowardAbrams
        - https://www.youtube.com/watch?v=L1f2tulD9N8&ab_channel=ProtesilaosStavrouProtesilaosStavrou

    - Emacs from scratch #1
        - https://www.youtube.com/watch?v=74zOY-vgkyw
* Lisp documentation 
    - https://www.gnu.org/software/emacs/manual/html_node/eintr/index.html#Top

# GOAL 

- goal of learning emacs is to understand mechanism behind how packages works. NOT LEARNING TO SWITCH TO EMACS. (I have decided on 6/22/2021 to not switch to emacs because it doesn't worth the effort) 
    *  exception TODO manager which I should completely switch to org-mode from markdown.

# TODO 

* here> Ultimate Goal: use emacs to create an app that can perfectly express by Garun workflow 
    * note
        - to enable automation of extract, deliver, storing.

    * learn how to configure emacs configuration
        * how to change config.el to .org
            * what does it mean by export source code?
            * here> what is relation betwen .doom.d and .emacs?
        * https://www.youtube.com/watch?v=74zOY-vgkyw&list=PLEoMzSkcN8oPH1au7H6B7bBJ4ZO7BXjSZ&ab_channel=SystemCrafters
            * what is straight.el?
            * here> read the following 
                * what is cookies?
                * package management in doom
                    * https://github.com/hlissner/doom-emacs/blob/develop/docs/getting_started.org#package-management
                        * what is package!?
                             * how to defind macros?
        * how to deal with error in emacs ?
        * evaluate elsip on the fly
            * error
                * not found [lisp] language information
    * goal: install smooth-scrolling.el  
        * ref
            * https://github.com/aspiers/smooth-scrolling 

    * here> goal: use scimax + doom emacs 
        * ref 
            * https://sqrtminusone.xyz/posts/2021-05-01-org-python/
            * https://dotemacs.readthedocs.io/en/latest/
        * here> scimax + doom?
            * here> just load packages used in scimax to doom. 
                * here> read https://sqrtminusone.xyz/posts/2021-05-01-org-python/
                    * here> emacs-jupyter vs ob-ipython vs emacs-ipython-notebook (ein)
                        * here> what does add-hook actually do?
                            * here> understand hook and flag
                                * symbols vs variables vs objects?
                                    * what is interns?
                                        * what is canonical symbol?
                                            * what does lisp reader do?
                                                * what are different things that are being processed in the "read" vs " eval" phases of lisp excution.
                                                    * what is obarray?
                                                        * https://www.gnu.org/software/emacs/manual/html_node/elisp/Creating-Symbols.html 
                                                            * command loop?
                                                                * change cursor insert mode.
                                                                * what is tellescope?
                                                                * what is treesitter?
                                                                * what is lsp?
                * what ppackages do scimax use?
                    * https://github.comtchin/scimax/blob/master/scimax.org/
                    * https://github.comtchin/scimax/blob/master/scimax-ipython.org/
        * make it better than vim 
            * here> do what vim does well 
                * here> lets make python IDE
                    * here> https://www.youtube.com/watch?v=6BlTGPsjGJk&ab_channel=thoughtbot
                    * https://www.youtube.com/watch?v=jPXIP46BnNA&ab_channel=SystemCrafters
                    * https://www.youtube.com/watch?v=E-NAM9U5JYE&list=PLEoMzSkcN8oNvsrtk_iZSb94krGRofFjN&ab_channel=SystemCrafters
                * writing research paper (latex)
            * expands beyound vim
                * interact with web browser
                * remote work with TRAMP
    * learn to use bash command with emacs
        * https://www.youtube.com/watch?v=3vQYHJ_RvjI&ab_channel=SahasSubramanian
    * Project: learn to build emacs pacakges from scratch 
        * https://www.youtube.com/watch?v=EqgkAUHw0Yc&ab_channel=SystemCrafters
            * continues at 53.35 am: start using lisp to interact with dot files
    - lets build emacs from scratch.
        * requirement
            * lets use emacs for window for this.
            - know what packages doom has add?
                - learn the following 
                    - treemacs 
                    - projectile
            * know how doom emacss communicate with emacs?
    * Project: lets recreate org-roam (to be like roam research)
    * Project: learn how emacs connects to external tools 
        * see reference for workflow that I want to know how it works
            * pdftools
                * dependency 
                    * needs to learn latex first

