# TERMINOLOGY
* todo manager 
    * todo manager manages order of todo files where todo files itself manage order of "action"
* action
    * actions is simply a task but re-write to describe the exact action needed to complete the task   
* Terminology
    * Terminology contains list of vocab that required for reader to understand the current file he/she is reading.

# TODO-MANAGER REPO
* description:
    * This repo manage todo using version control provided by git. 
    * TODO-MANAGER REPO manage todo list systematically and follow software engineering principle including 
        * single responsiblity principle
        * coupling vs cohesion

* Pros/Cons
    * Pros
        * managing todo list in this allows me to "pause" and "resume" on the exact "action" I was taking.
        * this TODO-MANAGER is created to help ease collaboration and enhance transparency in working environment.
        * looking git commit show amount of "action" I finished on each day.
            * using "git crawler" technique (don't remember the actual name) I can later plot "activity" graph for daily/weekly/monthly/yearly.
                * "git crawler"
                    * crawl git "diff" over time. 
                * this allows for easier goal setting for both long term and short term.
        * portability

    * Cons

* note:
    * each todo file should help reduce friction for collaboration.
        * example:
            * example 1
                * 3 people working in the same same projects. each members can create todo list to shared to other members, 
                 so all the members knows when there are updated to member's todo list. 
                    * This should reveal action (task) with incorrect priority, and, as a result, actions should be rearranged such that all members todo list are aligned with the team goal.
* naming convension:
    * Note
        * all names descibe under naming convension will follow regex rules.
    * file naming convension
        * \*\_todo\_manager 
            * description:
                * todo\_manager manage order of todo files where todo files itself manage order of "action"
            * example: 
                * PhDTODOs/PhD\_todo\_manager manages todo for todo files inside of PhDTODOs folder
* list of files worth mentioning
    * today's todo.txt
        * description:
            * the main todo manager (todo manager of all todo manager)
            * when action is complete, looking at today's todo.txt should route you to the next actions you need to do.
    * scrach.md
        * description:
            * scratch.md should not be version controled, but I am too lazy to get rid of it.
            * scratch.md is just a file that I just to put some random stuff in. I find myself needing this type of files so I figure
                to put it here as well 
    * hotkeys.md
        * description:
            * list of short cut keys across different apps. 
            * I find this super useful. because only noob uses mouse.
    * life\_events\_todo.md
        * description:
            * I shouldn't version control this, but my parents want to know what i am up to, so they can have a look whenever they want.
