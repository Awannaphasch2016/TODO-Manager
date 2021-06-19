# TODO
* 

* here> emacs rabbit hole
    * note
        * usecase
            * org-mode usecase 
                * daily journal + calenday
                    * https://www.youtube.com/watch?v=3V3wIJgMeqE
                * pdf-tools workflow 
                    * note
                        * annotation on pdf (pretty cool)
                    * https://www.youtube.com/watch?v=LFO2UbzbZhA
            * swithcing from vim to emas in 20 mins 
                * https://www.youtube.com/watch?v=V27zOhfN8Ys
            * replacing terminal based program with emacs
                * https://www.youtube.com/watch?v=HzFqZ0Gl0aw
            * list of exapmles on using emac with tmux
                * https://www.reddit.com/r/emacs/comments/5j89xn/tmux_emacs/
            * chrome + emac
                * https://www.youtube.com/watch?v=wyPZws66Sic
                    * atomic chrome
            * emac + data science
                * https://ahsanijaz.github.io/2016-09-20-Emacs/
            * emacs for math
                * https://www.reddit.com/r/emacs/comments/jacnfq/emacs_and_math/
            * emacs agenda workflow 
                * https://blog.aaronbieber.com/2016/09/24/an-agenda-for-life-with-org-mode.html
                * http://cachestocaches.com/2016/9/my-workflow-org-agenda/
        * tutorial 
            * here> Emacs from scratch #1
                * https://www.youtube.com/watch?v=74zOY-vgkyw
            * git
                * here> https://github.com/nobiot/Zero-to-Emacs-and-Org-roam
    * todo
        * here> try to replace roam research with org-roam?
            * read minor modes 
                * https://www.gnu.org/software/emacs/manual/html_node/emacs/Minor-Modes.html
            * read major mode
                * https://www.gnu.org/software/emacs/manual/html_node/elisp/Major-Modes.html
            * here> watch https://www.youtube.com/watch?v=GK3fij-D1G8&ab_channel=NiklasCarlsson
                * here> read basic of emacs  
                    * https://www.gnu.org/software/emacs/manual/html_node/eintr/index.html#Top
                        * here> list processing
                            * https://www.gnu.org/software/emacs/manual/html_node/eintr/List-Processing.html
                        * writing defuns
                        * buffer walk through
                        * more complex
                        * narrowing & widening
                        * readying a graph
                        * 
                * what are packages doom adds?
                    * learn the following 
                        * treemacs 
                        * projectile
        * replace todo manager with org-mode?
        * connect emacs to external tools. 
            * to enable automation of extract, deliver, storing.
        * try the following 
            * daily journal + calenday
                * https://www.youtube.com/watch?v=3V3wIJgMeqE
            * pdf-tools workflow 
                * note
                        * annotation on pdf (pretty cool)
        * list of things to learn
            * ref 
                * https://www.quora.com/What-are-good-ways-to-migrate-from-vim-to-emacs
            * Learn the basics text navigation commands (C-p, C-n,C-f,C-n,C-a,C-s)
            * Learn the basic management commands (C-x-f,C-x-s,C-x-b)
            * Learn macro commands to edit stuff like multiple cursors mode in Sublime (C-x-(,C-x-),F4)
            * here> Learn your major mode commands
            * For Clojure Cider it is: (C-x-e,C-c-M-j,C-c-z,C-c-M-c)
            * For Paredit it is C-)
            * Learn M-x command for anything else
            * You are good to go. ~3 days is enough to fully transition to Emacs.
            * learn lisp to read configuration.
        * can or should I replace all vim configuration with emacs?

* create UltiSnips for latex for the following
    * tables
    * citation

* research util
    * latex stuff
        * todo 
            * autocomplete works, but markdown (not Rmarkdown) doesn't generate citation when compile
                with pandoc
                * generate citation with pandoc
                    * https://v4.chriskrycho.com/2015/academic-markdown-and-citations.html
        * here> can I convert pdf to bib?
            * ref
                * here> https://github.com/perrette/papers
                * https://www.youtube.com/watch?v=nO4T8JDNYG0
        * figure out hwo to use vim-pandoc to get citation.
        * are there linux command for researchers who read and write lots of papers?
        * how to add program as cli.
        * learn to use RMarkdown in vim 
            * https://github.com/vim-pandoc/vim-rmarkdown
    * automate getting citation (such as bibtex)
        * requirement
            * from list of pdf, it can generate list of citation
            * from list of name, it can generate list of citation
        * here> just follow this shit https://www.youtube.com/watch?v=nXgqnYVAzKk
            * use and read his script. 
        * create commandline to get bibtex.
            * see section bibtex in https://scholarly.readthedocs.io/en/latest/quickstart.html#usage 
                * error
                    * limit by google scholar maxmimum try which is low af
            * use doi to pdf
                * note
                    * this requirement you to load pdf to local.

* space repetition 
    * here> [selected] test neuralcache with roam 
        * how to connect iphone to computer?

    * anki-vim 
        * error
            * here> Anki error
                * ref
                    * anki + vim
                        * https://sofiabelen.github.io/blog/anki-vim.html
                * front of this card is blank 
                    * I believe that this error is caused by styling, so see how to style anki
                    * note
                        * both side of the cards 
                    * attempted
                        * reinstall doesn't help. Preferences and setting seems to be remembered from
                            the first installed.
            * X11 error
                * error:
                    X Error of failed request:  BadDrawable (invalid Pixmap or Window parameter)
                      Major opcode of failed request:  14 (X_GetGeometry)
                      Resource id in failed request:  0x1
                      Serial number of failed request:  8
                      Current serial number in output stream:  8
                * attempted
                    * can I run X_GetGeometry?
                    * where is xorg.conf?
                        * do i use xorg server?
                    * how does scrot work?
                        * how does scrot use QT?
                    * can I run other QT application?
                        * what are other QT application for linux ?
                  * QT_X11_NO_MITSHM – stops Qt form using the MIT-SHM X11 extension.
                        * QT
                            * here> how does Qt create a window?
                            * Qt and wsl?
                        * what is MIT-SHM X11 extension?
                            * Can x server sue regular virtual meemry of pixmap ?
                        * ref
                            * https://en.wikipedia.org/wiki/MIT-SHM
                            *
                            https://forums.xilinx.com/t5/Design-Entry/X-Server-Error-Message-reported-is-BadDrawable-invalid-Pixmap-or/td-p/357153
                        * what is QT?
                            * here> https://en.wikipedia.org/wiki/Qt_(software)
                        * here> look into scrot code to see what cause the error
                            * ref
                                *

                                https://www.cyberciti.biz/faq/how-to-get-source-code-of-package-using-the-apt-command-on-debian-or-ubuntu/
                                * can't install .deb file on Ubuntu
                                    *
                                    https://www.ubuntupit.com/cant-install-deb-files-ubuntu-heres-possible-ways-install-deb-packages/
                            * C language program 


    * check if I need anything else other than 
        * picture 
        * ultraSnips
    * how to open file for edi
        * create my own UltraSnips
        * learn UltraSnips for 
