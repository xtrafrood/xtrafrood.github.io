---
title: 💻 Git Quick Ref.
author: Chris Schammert (csmertx -- Christopher Schammert )
published: 2023-01-31
weight: -20
---

<!-- The content of this website was written by Christopher Schammert aka Chris Schammert -->

<br />

> Just enough to be dangerous

## Basic push to origin

- ```echo $PWD```

    > Current dir the project dir? Great. Continue..

    > No? Then ```cd ~/.sources/projectdirectory```. See Bash prompt links [below](#resources)

- ```git add .```

    > Or: ```git add example1.sh```

- ```git commit -m "commit message"```

- ```git pull```

- ```git push -u origin```

## Remove all traces of sensitive data from a repo

> This won't remove it from clones or forks, but at least the repo will be scrubbed

- BFG Repo-Cleaner linked [below](#resources)

- ```vim ~/.bashrc```

    ```
    ++ alias bfg='java -jar ~/.sources/bfg-1.14.0.jar'
    ```

- ```source ~/.bashrc```

    > ```bgf``` via new Bash prompts 

- ```echo "sensitive_data_to_be_removed" >> ~/passwords.txt```

    > OR: ```echo -en "data1\ndata2\ndata3" >> ~/passwords.txt```

- ```cd ~/.sources/gitrepo```

    > This will obviously work better in the repo directory

- ```bfg --replace-text ~/passwords.txt```

    > Crucial step to clear repo history of that data

- ```git reflog expire --expire=now --all && git gc --prune=now --aggressive```

    > ```bfg``` should prompt you to issue the the above command

- ```git push --force```

    > That should do it. Good luck!

## Resources

- [Git: Bash Prompt](https://www.git-scm.com/book/en/v2/Appendix-A%3A-Git-in-Other-Environments-Git-in-Bash)

- [Easy Bash PS1 (Prompt) Generator](https://ezprompt.net/)

- [Github Docs: Removing sensitive data from a repository](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository)

- [BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/)

<br />

<div style="text-align: center; font-size:12px; color:dimgray">
    Created: 12/29/2021 • Edited: 02/09/2025 • Author: Chris Schammert (csmertx) • 
    <a href="https://github.com/csmertx/csmertx.github.io/commits/main/content/Linux/Code/github_quick.md" 
       title="Github.com | csmertx \ csmertx.github.io \ commits \ main \ content \ Linux \ Code \ Git Quick Ref.">
       History 🕵️
    </a>
</div>