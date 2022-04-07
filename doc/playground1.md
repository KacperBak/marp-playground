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
| **Nr.** | **left alignment**         | **center alignment** | **right alignment**            |
|---------|----------------------------|:--------------------:|-------------------------------:|
| 1       |_italic_                    |->                    | \_italic\_                     |
| 2       |**bold**                    |->                    | \*\*bold\*\*                   |
| 3       |`code`                      |->                    | \`code\`                       |
| 4       |[Link](https://source.org/) |->                    | \[Text\]\(https://source.org/\ |             


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

<!--
- It's like styling a website
- but, don't ask me how to center a div
-->

> In that case the style of this deck is overloaded.

---
# Image Custom
Embed an image fit to custom size using `width` and `height` attributes:

```Markdown
![w:320 h:320](./img/bliss.jpg)
```

![w:320 h:320](./img/bliss.jpg)

---
# Image Filter

<style scoped> 

p {
  text-align: center;
}
</style>

![sepia w:800 h:600](./img/bliss.jpg)



---
![bg](./img/bliss.jpg)
# Background 
<style scoped> 

h1, p {
  color: white
}
</style>
...
Scale bg image to fill the slide is the `default` case

---
![bg left](./img/bliss.jpg)
# Background Left

...
Background using left side


---
![bg left:33% grayscale](./img/bliss.jpg)
# Background Left

...
Background using `33%` of the left side with `grayscale` filter



---
# Export Options

- **PDF** to **share** slide deck with others
- **HTML** to **present** slide deck to others
- **HTML** to **host** slide deck as a web page
- **PPTX** to **edit** it further with PowerPoint, but with READONLY content!

---
![bg left grayscale](./img/bliss.jpg)
# Presentation Notes

define handy presentation notes using html comments:

```
<!-- 
- my notes 1 
- my notes 2
- my notes 3 
-->
```


---
# PRO's
- define your presentation in `Markdown` and leverage your existing for source code tooling
  - use <your-fav-editor> instead of products like KeyNote, PowerPoint, Impress, ...
  - versioning, diffing, etc.
  - grep over content, search & replace etc.
- useful export options: ``PDF``, ``HTML``, ``PPTX``
- define your style in a common CSS way
- define handy presentation notes using html comments: `<!-- my notes -->` 


<!-- 
my notes 1 
my notes 2
my notes 3 
-->
---
# CON's
- Editing and formatting like `change size, rotate, positioning` of images is partially supported by directives.
- To deal with images `directives` need to be known.
- No drag & drop support for images
- No helper tools like arrows, rectangles shapes, etc.

<!--
- NOT so intuitive like in classic GUI tools like PowerPoint, KeyNote etc.
- Directives need to be learned
-->
---
# Conclusion
It's more like building a very simple **html** page.

# Use case
Generate project data results from your CI/CD into a slide deck.

---
# Sources
- https://marp.app/
- https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode
- https://marpit.marp.app/directives