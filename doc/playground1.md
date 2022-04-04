---
marp: true

---
<style>
:root {
  background: #FFFFFF
}

h1, h2, h3 {
  color: #780000
}

</style>

# Use Common Markdown 

# h1 - heading 1
bla
## h2 - heading 2
bla bla 
### h3 - heading 3
bla bla bla


---

# Tables
| **Nr.** | **left alignment**         | **center alignment** | **right alignment** |
|---------|----------------------------|:--------------------:|--------------------:|
| 1       |_italic_                    |->                    | \_italic\_           |
| 2       |**bold**                    |->                    | \*\*bold\*\*         |
| 3       |`code`                      |->                    | \`code\`             |
| 4       |[Link](https://source.org/) |->                    | \[Text\]\(https://source.org/\)|             


---

# Numbered Lists
1. asdf ....
   1. asdf ....
      1. asdf ....
         1. asdf ....
         2. asdf ....
         2. asdf ....
      2. asdf ....
   2. asdf ....
2. asdf ....
4. asdf ....

--- 
# Code highlighting

```java
public class App {

    private static final String VERBOSE_KEY = "stdout";
    private static final String VERBOSE_VALUE = "verbose";
    private static final int PAUSE_IN_MS = 2000;

    public static void main(String[] args) {

        // To display the thread implications on stdout set the property to 'verbose'
        System.setProperty(VERBOSE_KEY, VERBOSE_VALUE);
        try {
            var app = new App();
            var result = app.usingWhenComplete().get();
            System.out.println(result);
        } catch (Exception e) {
            System.out.println(e);
        }
    }
}
```

--- 
# Set your Style like in CSS
<style scoped>
section{
     background: magenta
     
}   

h1 {
  color: yellow
}

p {
    color: white
}
</style>


```CSS
<style scoped>
section{
     background: red
}   

h1 {
  color: yellow
}
</style>
```

> In that case the style of this deck is overloaded.


---
# PRO's
- define your presentation in `Markdown` and leverage your existing for source code tooling
  - use <your-fav-editor> instead of products like KeyNote, PowerPoint, Impress, ...
  - versioning, diffing, etc.
  - grep over content, search & replace etc.

- export to
  - **PDF** to **share** slide deck with others
  - **HTML** to **present** slide deck to others
  - **HTML** to **host** slide deck as a web page

- define your style in a common CSS way
- define presentation notes using html comments: `<!-- my notes -->` 


<!-- 
my notes 1 
my notes 2
my notes 3 
-->
---
# CON's
- Formatting images is complicated
- No helper tools like arrows, rectangles shapes, etc.

---
# Use case
Generate project data results from your CI/CD into a slide deck.

---
# Sources
- https://marp.app/
- https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode
- https://marpit.marp.app/directives