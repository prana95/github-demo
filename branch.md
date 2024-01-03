# Branch

## To delete 
to delete a branch -> git branch -d name_of_branch

## To rename
to rename a branch -> git branch -m source_name destination_name

## fast forwarding while merging a barnch
imagine if I have a branching like this 

new_branch ->	a1--a2---a3
		|
main ->  c1--c2--

if there is a git merge new_branch on a main branch the branching will go like this 

main -> c1--c2--a1--a2--a3

this is called fart forwading if there is no commit in the main branch after creating a new branch and if we  merge the new branch to main there will be a fast forwading merge 
cf:https://capgemini.udemy.com/course/git-complete/learn/lecture/1955638#overview

# To disable the fast forwading while merging branches

new_branch ->	a1--a2---a3
		|	  |
main ->  c1----c2----------z1

here z1 will be the new node of the branching. to achive it while merging we need to give the --no-ff  which means NO FAST FORWADING

so the command will be -> git merge new_branch --no-ff
this command will merge and ask the commit message 

# normal merging with lots of commit

new_branch ->	a1--a2---a3
		|	  \
main ->  c1--c2----c3--c4--z1

same one but main has commits parallel to the main branch
command to merge (checkout to the main branch): git merge new_branch -m "a commit message so it wont redirect to the vim or other editor" 

