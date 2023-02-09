# Integrated Terminal - A powerful feature!

VS Code provides a full-fledged terminal that starts at the root of the workspace.

To open the terminal:

* Use the ⌃\` keyboard shortcut to toggle the terminal panel.
    
* Use the ⌃⇧\` keyboard shortcut to create a new terminal.
    
* Use the View &gt; Terminal or Terminal &gt; New Terminal menu commands.
    
* From the Command Palette (⇧⌘P), use the View: Toggle Terminal command.
    

![Terminal Image](https://cdn.hashnode.com/res/hashnode/image/upload/v1675914671532/9ed1edf4-ae9d-41a8-97c8-dedde42d9b14.png align="left")

You can open a new terminal session directly in VS Code in your working directory using `ctrl+ backtick` (the key below the escape key).

When you start your terminal it uses your default shell, if you click on the caret it will show you a list of shells you can use if needed.

![Shells](https://cdn.hashnode.com/res/hashnode/image/upload/v1675914673300/72ac43e9-ece6-4717-8008-bfcac732b914.png align="left")

What often happens though is you may need multiple terminal sessions running at the same time. Like one for your server and the other for managing git or tests.

You can also change the name, color, and icon of that terminal session, right click on the terminal session you want to change the information for you may see these options

![terminal sessions](https://cdn.hashnode.com/res/hashnode/image/upload/v1675914675871/c3291c42-aec4-49fe-b8ea-ad2937450428.png align="left")

Click on change color, different color options may appear in the command palette.

![terminal info](https://cdn.hashnode.com/res/hashnode/image/upload/v1675914677505/da864dbc-ade3-4cb2-8787-aa1240ce1e2c.png align="left")

![terminal info](https://cdn.hashnode.com/res/hashnode/image/upload/v1675914678610/080b7202-11bb-416a-82b3-059d8b528826.png align="left")

Similarly, you can change the icon, name, color, etc. And now you need to fumble between the different terminals to figure out what each one is doing.

Now if you type out an actual command in the terminal and you screw it up you can use control + arrows(right|left) to navigate through the command your mouse won't even work here. You can clear the terminal using `ctrl|cmd + k` then use up arrow to go to the last command in your history.

## Tasks

What if there is a way where you don't have to write the same command over and over again in the same terminal? Like how many times you might have written `npm start` or `npm run dev` to simplify, you can create a VS Code task, a JSON configuration that contains the commands you want to run in the terminal.

### Create a task

* Go to the command palette `ctrl|cmd + shift + p`
    
* write task
    
* select configure default build task
    

![vs code tasks](https://cdn.hashnode.com/res/hashnode/image/upload/v1675914679674/a0c73bdd-5188-4486-9087-381c1360f352.png align="left")

![vs code tasks](https://cdn.hashnode.com/res/hashnode/image/upload/v1675914681293/701cc463-158c-4bf8-bd40-713f2112bb8c.png align="left")

![vs code tasks](https://cdn.hashnode.com/res/hashnode/image/upload/v1675914682874/af2e9fb7-d813-4247-b738-6e41528ab1ef.png align="left")

![vs Code tasks](https://cdn.hashnode.com/res/hashnode/image/upload/v1675914684040/120bdba6-1a8d-4e3d-954d-71de753fddf7.png align="left")

All these powerful features may help you boost your productivity while coding. Let me know in the comments below the productivity hack you use to increase your productivity.

#### Want to connect?

[twitter](https://twitter.com/garimaasharma_) · [blogs](https://dev.to/garimasharma) · [portfolio](https://garimasharma.netlify.app) · [email](mailto:sharmagarima814@gmail.com) · [linkedin](https://www.linkedin.com/in/garima-sharma08/)