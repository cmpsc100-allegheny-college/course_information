# CMPSC 100: Workflow Resources

![Pixelated desert with tumbleweeds, birds circling, at high noon](https://raw.githubusercontent.com/allegheny-college-cmpsc-100-fall-2022/course-materials/media/media/term_desert.png)

Here you can find the tools needed to traverse and use `term-world`.

# Table of Contents

- [SSH Keys](#ssh-keys)
- [Getting Content](#getting-content)
- [Common Commands](#common-commands)
  * [cd](#cd)
  * [ls](#ls)
  * [tree](#tree)
  * [python](#python)
- [Inventory](#inventory)
  * [get](#get)
  * [use](#use)
  * [remove](#remove)
  * [drop](#drop)
- [Checking Out Branches](#checking-out-branches)
- [Pulling and Updating Content](#pulling-and-updating-content)
- [Evaluating Content with Gatorgrade](#evaluating-content-with-gatorgrade)
- [Submitting or Saving Content](#submitting-or-saving-content)
  * [Merging Content](#merging-content)
- [Collaborative reflections](#collaborative-reflections)
- [Making an improvement proposal](#making-an-improvement-proposal)
- [Backup Policy](#backup-policy)

## SSH Keys

After creating a `Github` account, you will need to create a `SSH` key in order to authenicate your account in `term-world`. Here is a video detailing the process:

[![SSH Key video]( http://img.youtube.com/vi/qEPjUGQFmzQ/hqdefault.jpg)](https://www.youtube.com/watch?v=qEPjUGQFmzQ&list=PLsYZRXov75ZHSwWiCk0-jd1RcTuu_-zmD&index=1)

## Getting Content

In order to complete the workload for any project you'll first need to `clone` the repository into `term-world`.

When you `clone` a repository you're duplicating its contents and adding them to your local workspace (e.g., your `term-world` browser) where you can safely edit the contents of the repository as needed.

This time around, we will `clone` our repositories. This is the way we'll interact with `git` and GitHub for the remainder of the semester. We can consider a `clone` as something that's part download, part direct link. It's a similar relationship between that of GitHub, `term-world`, and our `house`.

The process has two (2) major parts.

### GitHub

- On your GitHub assignment page (i.e. _this_ page) locate the green `Code` button
- Select the `SSH` link from options presented
- `Copy` or click the button at the far right of the textbox on that screen

![TW - Clone link diagram](https://user-images.githubusercontent.com/1552764/213940345-2e62ec2e-e017-40ff-b325-745f9e731041.png)

### `term-world`

![TW - Clone Repo](https://user-images.githubusercontent.com/1552764/213931807-993be051-59e4-4102-b183-8c65bacaadee.png)

- In `term-world`, find the `Source Control` menu
- Locate and click the `...` at the top right of the window
- Choose `Clone` from the list of options
- Paste the link copied above
- Choose your home folder as the location into which to clone the repository

## Common Commands

In order to navigate around the files and folders during each project in `term-world`, there are a few commands you will need.

### cd

`cd` is short for "change directory"; this command allows you to move to different folders in the directory `tree`.

![House assignment as tree structure from top to bottom with home directory at top](https://raw.githubusercontent.com/term-world/syllabus-template/media/img/TW%20-%20Folder%20Tree.png)

For Example, if we were in folder `house` of the above directory `tree` we would use the following command to move to the `living-room` folder:

```
cd living-room
```

Then if we wanted to go back to folder `house` we would use the command:

```
cd ..
```

We can even chain these commands together to move multiple folders at a time, such as if we wanted to move directly to folder `dining-room` from folder `house`:

```
cd living-room/dining-room
```

In order to check where you are in `term-world` you can always check your `command prompt` from the text right before your cursor. If we were in folder `B` for example, we might see:

```
cliv3@term-world:~/house/living-room$ 
```

Here we can see that we are in folder `living-room`, which is inside of folder `house`, which is in our _home_ directory (which is indicated by the `~`).

### ls

Anytime you wish to "list" out the contents of a given folder you can use the command `ls`; this will list out all folder and files in a given folder. If we were to run the `ls` command from folder `living-room`, for example:

```
cliv3@term-world:~/house/living-room$ ls
hallway  dining-room
```

Here we can see that the two folders belonging to `living-room` (`hallway` & `dining-room`) are produced as output from the `ls` command. This is handy for knowing what navigation options are available to you at any time.

### tree

The `tree` command will display the contents of the files and subfiles at your current location. This command is very useful for when you want to see all the files without using `ls` multiple times.

### python

If you want to run the code inside of any Python file (which are generally indicated with a `.py` extension at the end of the file name), you simply use the `python` command. For this particular command, you need to follow the command itself with the full file name, all on a single line. For instance, if I wanted to run a program called `Box.py`, I would use the command:

```
python Box.py
```

Of course, this command has to be run in the directory that houses the Python file. `ls` is helpful for knowing if you're in the right place to run the `python` command!

## Inventory

`inventory` is a command that is used to carry different objects around `term-world`. You can only carry `10` objects with `inventory` (objects have varying weights).  In order to check whats in your inventory use the command:

```
inventory
```

You will see a screen similar to that below:
![Inventory screen showing three items](https://raw.githubusercontent.com/allegheny-college-cmpsc-100-spr-2023/course-materials/media/img/TW%20-%20Inventory.png)

### get 

`get` picks up an object from your current location. This commands destroys the objects in its current location. Make sure to use the **file name**.

```
get Tomato.py
```

### use

If the object is `Consumable`, you can use the `use` command to "use" the object. If It does not have any function then `use` just removes the file. Only uses `1` object at a time.

```
use Tomato
```

### remove

`remove` gets rid of an object from your `inventory`. You first use the name of the object, then you give the amount of objects you want to delete (If no amount is given then 1 is removed). If you give an amount higher then you have, all objects are removed.

```
remove Tomato 2
```

### drop

`drop` puts the object in your current location. You first use the name of the object, then you give the amount of objects you want to drop (If no amount is given then 1 is dropped). If you give an amount higher then you have, all objects are droped.

```
drop Tomato 3
```

This command will drop `3` `Tomato.py` files. This is how the files would be dropped:

```
Tomato.py
Tomato1.py
Tomato2.py
```

If any more files are dropped they will continue to follow this numbering pattern. Picking up any of these files will give you a `Tomato` in your inventory.

## Checking Out Branches

When working on `term-world` content, you'll often need to create a new test `branch` in order to get get feedback and make corrections before altering the `main` branch's code. 

There are multiple ways to do this but the easiest way is to click on the `branches` button in a `Github` repository then clicking on the green `create branch` button. Then you can name that branch and create it. 

From there you can go back to `term-world` and use the terminal to type the following command:

```
git fetch
```

This will fetch new branches that were just created in `Github`. Then in order to change over to our newly made branch we will use the command:

```
git checkout NEW-BRANCH-NAME-HERE
```

This will switch us over to the new branch and allow us to safely code without the chance of breaking the `main` branch

In case you forgot what branch you are in you can use the command:

```
git branch
```

This will display your current branch as well as any other branch that may have been created in this repository.

## Pulling and Updating Content

When changes are made to `main` by you or your group members, you will need to `pull` those changes to `term-world` from `GitHub`. In order to pull new content from `main` or any other branch you first need to use the `git checkout` command to switch to the branch you want to update. Once there, simply use the command:

```
git pull
```

## Evaluating Content with Gatorgrade

Each week's repository is outfitted with a grader that can be used to evaluate your work for the week. In order to run the this grader for a given week's work, you'll need to first navigate to the "root" folder of the assignment (that is, the base folder containing a given assignment's work, such as `house`):

```
cd ~/house
```

Once there you'll need to run the following command:

```
gatorgrade
```

Once the grader has finished running (it may take a couple minutes) you'll be presented with a series of checks that determine the overall "completeness" of your work. For instance, your output may look something like:

```
✔  Customize the nameplate (no TODOs)
✘  Find the Ink hidden in the couch
✘  Print the lease
✔  Enter the house
✘  Open the UltraHeavyBox
✘  Open the FragileBox
✘  Open the SinisterLookingBox
✘  Open the TubeShapedBox
✘  Open the BeatUpBox

-~-  FAILURES  -~-

✘  Find the Ink hidden in the couch
✘  Print the lease
✘  Open the UltraHeavyBox
✘  Open the FragileBox
✘  Open the SinisterLookingBox
✘  Open the TubeShapedBox
✘  Open the BeatUpBox

        Passed 2/9 (22%) of checks for user-house-solved! ┃

```

As you can tell, there are some checks which have been satisfied, though there are many which have not. Be sure to have *all* of the required checks completed by the due date in order to receive credit for assignment completion!

## Submitting or Saving Content

The GitHub platform is a place to store your work. So, it makes some sense that should be able to download from it, and push back (upload) to it. Here, we'll learn this second part.

Bottom line: we need to tell git that there have been changes.

Observe the list of files you've changed and add them to a staging area using the + button to the right of each file
Once these have been "staged," attach a message to what we call a commit -- a "packaging" of the files to send to GitHub.

To follow this process:

![TW - Commit and Sync](https://user-images.githubusercontent.com/1552764/213940290-23b12a8a-6283-492c-ab1c-66a801ba815e.png)

To complete the process you'll need to input the password associated with your `SSH` key.

### Branched Content

If you pushed content to a branch away from `main`, you can now make a `Pull-request` in `GitHub` by clicking on the `Pull-request` tab and creating a new `Pull-request` that compares your branch to `main`. From there you can evaulate the changes made and `merge` your branch with main.

* If this is a group project then you will need the approval of your group members before you can merge. This is done by assigning your group members to the `Reviewers` tab towards the righthand side of the `Pull-request` page.

### Merging Content

In some cases when you make a pull request you'll have to specify what parts of a pull request make it into the `main` branch. If that's the case, you'll instead see a `Resolve conflicts` button. Click that and you'll be presented with a proposed merged copy of the code, with some extra lines added in. Something akin to:

```
<<<<<<
x = "this_is_a_line_of_code"
=======
x = "this_is_a_different_line_of_code"
>>>>>>
```

To resolve said conflicts, you'll need to delete the portion of code you don't want to appear in the final product, as well as any `<<<<<`, `======`, or `>>>>>>` lines.

Once complete, click `Mark as resolved` followed by `Commit merge`, and the changes on the branch will be joined with the `main` branch!

## Collaborative reflections

On many group assignments there will be a `reflection` file. After the assignment is completed, each member of your group will respond to questions posed about the assignment. To do this your group should create one branch called `reflection` to capture your work on this section of the assignment; all members should contribute to the same branch.

## Making an improvement proposal

This assignment begins your opportunity to propose and improve the world of `term-world` at-large. For this assignment, proposals may include making graphics to improve the `bodega` site experience, creating new items or actions in the `traffic-circle` itself or another assignment-related improvement not contemplated in the prior narrow categories.

To make an improvement proposal, you must _create an issue_ on this repository. Do so by:

* clicking the `Issues` tab at the top of the page.
* clicking the green `New Issue` button
* selecting the `Improvement Proposal` template 

**Make sure to link your issue with the pull request you used to make your actually improvement.**

**If you are not following an improvement suggestion you need to have your improvement suggestion checked by the professor before proceeding.**

## Backup Policy 

**While we may use this server to store code, you are responsible for using GitHub as your main backup.**

In the event that the `term-world` server goes down for any unforeseen reason, your work may be lost. Though this server is backed up on a regular (i.e. weekly) basis, there is no guarantee that up-to-the-minute data for your work will be restored.

Remember: to err is human; to back up your work is *divine*.
