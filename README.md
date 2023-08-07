# Github tricks and tips 

### Remove Connection From Git:
Sometimes when your creating a project if your using npx etc.. that project might create a connection to a git repository:
> You can tell because you will see (master) when your in the project folder.

Now when you come to push that project to your own repo your gonna get an error. So what you need to do is remove that connection in your project before adding it to your repository.

```bash 
rm -rf .git
```
run this in your project folder and you should be fine. This command removes the `git` connection from that project. You wont get any errors now when adding your project to your `github`.

### Removing Pushed Packages

If you already pushed up your node_modules, adding it to .gitignore wont do anything, its already pushed my guy. if you want to remove there is a few steps you need to walk through.

1. `git rm node_modules` locally 
2. commit changes to local repository
3. run `npm install` to re-create `node_modules` folder
4. create  `.gitignore`
5. commit changes locally
6. push updates to  `github`

Example of how your `.gitignore` should looks is as simple as this :

*.gitignore*
```
/node_modules

```# Github-Tips
