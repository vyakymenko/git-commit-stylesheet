### Git Branches/Commit Style for Enterprise Development

## Introduction 

After I started working on large projects, I realized that it's rather problematic to track, make pull requests review, in a chaotic structure in any VCS, where everyone creates branches and commits as wants. After all, each of us tries to separate ourselves in a special way.

## Solution

I decided to create some kind of small system of conducting commits and branches in our company.

## Branches

I divided the structure of branches into 4 main subclasses:

-   `bugfix/{Ticket Number}-{Small ticket description}`

    Typically used for fixing bugs against a release branch.

-   `feature/{Ticket Number}-{Small ticket description}`

    Used for specific feature work. Typically, this branches from and merges back into the development branch.

-   `hotfix/{Ticket Number}-{Small ticket description}`

    Typically used to quickly fix the production branch.

-   `release/{Ticket Number}-{Small ticket description}`

    Used for release tasks and long-term maintenance. Typically, this branches from the development branch and changes are merged back into the development branch.

With this structure, I know exactly which type my task belongs to if everyone adheres to the system.

## Commits

Next, I came up with a certain system for creating commits, please note that according to my point of view there are only 2 types of commits, creation and updating ( fixing a bug is updating the created functionality from the previous commit(s) ). Therefore, I split the message messenger into 2 types with branching to levels using the `*` delimiter, you can use whatever you like (`#`) etc.:

-   `Implement` Example:
```
Implement:
    * Add todo functionality: 	
        ** Add todo.
        ** Todo list. 	
    * Change styles for view.
```

-   `Update` Example: 

```
Update: 
	* Update todo app functionality: 
	    ** Changed color of `Add` button.
	    ** Modify labels for todo list.
```

Such a structure of branches and commits helps to easily track changes in the entire team, switch between tasks, branches and do not waste time searching for a ticket and its description of what really needed to be done.


I hope this helps, thank you.


#### P.S.

Of course you can use same for other VCS.