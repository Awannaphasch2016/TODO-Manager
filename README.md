# TODO-MANAGER REPO

## DEFINTION
* This repo manage todo using version control provided by git. 
* TODO-MANAGER REPO manage todo list systematically and follow software engineering principle see BEST PRACTICES for more detail 
* labeling style follows "Garan - a shared knowledge repo."

## REQUIREMENTS
* note:
    * list of requirements is not exhausive 

### USER REQUIREMENTS
* a bullet point (todo action) is inserted only if user plan to remove it in the near or distance future
* managing todo list in TODO MANGER allows user to "pause" and "resume" on the exact "action" I was taking.
* TODO MANGER of a project manager should be able to track works of his/her employees.
    * note: 
        * this is still a work in progress i don't know if there exist a way to enfore privacy or scope. (to limit visibility of todo list to a certain group)
    * project manager update todo list to TODO MANAGER arange based on project (separated by folders)
    * an employee can send pull requests to project which he/she is responsible for. 
    * project manager approve/resolve pull request.

### SYSTEM REQUIREMENTS
* children bullet points must describe a parent bullet point which their belong to 
* bullet point of the same hierarchy level is equally important in priority. 
    * this implies reodering between bullet point of the level should not have any significant in term of time to complete parent bullet point.
* TODO MANAGER repo should allow for full transparency of what actions I have taken towards certains action/task/goal.
    * this implies that I cannot lie about what I have done unless I take my time to manupulate commit history which is a lot of work in itself, but this shouldn't be possible or extremely hard to manipulate. 
     This is because of the following 
        1. commit message is required to be updated daily 
            * daily actions is neatly version controled.
        2. commit message has timestamp.
            * to manipulate commit history, I need to align actioned taken daily with the actual date. 
        3. dashboard that tracked 'git show commit' is updated daily.
            * to manipulate commit history, I also need to be aware that there is no spike in actions taken on certain projects (direcotry/folder). This manipulation can be easily validated 
             by looking for weird action taken spike on the dashboard.
* each todo file should help reduce friction for collaboration.
    * example:
        * example 1
            * 3 people working in the same same projects. each members can create todo list to shared to other members, 
             so all the members knows when there are updated to member's todo list. 
                * This should reveal action (task) with incorrect priority, and, as a result, actions should be rearranged such that all members todo list are aligned with the team goal.

## TERMINOLOGY
* Terminology
    * Terminology contains list of vocab that required for reader to understand the current file he/she is reading.
* todo manager 
    * todo manager manages order of todo files where todo files itself manage order of "action"
* action
    * actions is simply a task but re-write to describe the exact action needed to complete the task   

### naming convension:
* Note
    * all names descibe under naming convension will follow regex rules.
* file naming convension
    * \*\_todo\_manager.md
        * description:
            * todo\_manager manage order of todo files where todo files itself manage order of "action"
        * example: 
            * PhDTODOs/PhD\_todo\_manager manages todo for todo files inside of PhDTODOs folder

### list of files worth mentioning
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
* note\_for\_code.md
    * description:
        * this file contain in a programming related projects. The code is as the name suggest to make note about the code.
            * this is often helpful to me because making on the code base lead to stupid merge conflict and hard to maintain or not read able when working on multiple project 
             at the same time OR "resume" actions on old projects/side projects.
            * this approach prevent you from having to write UML for the project or make intensive documentation on the project. Using 'node_for_code' all you need to care to take 
             note is the part of the code that confuse to you ( fortunately, your current you and your future you share the same studpid brain that required to understand the same code)

## BEST PRACTICES
* TODO MANAGER obeys the following software engineering principles
    * single responsiblity principle
    * coupling vs cohesion
* TODO list should be refactored whenever the following software engineering principles are violated
    

## Pros/Cons
* Pros
    * this TODO-MANAGER is created to help ease collaboration and enhance transparency in working environment.
    * managing todo list in this allows me to "pause" and "resume" on the exact "action" I was taking.
    * looking at git commit show amount of "action" I finished on each day.
        * using "git crawler" technique (don't remember the actual name) I can later plot "activity" graph for daily/weekly/monthly/yearly.
            * "git crawler"
                * crawl git "diff" over time. 
            * this allows for easier goal setting for both long term and short term.
    * portability

* Cons

