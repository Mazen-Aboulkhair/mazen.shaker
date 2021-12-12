## Usage of const keyword and "&" operator in c++

You can use the [editor on GitHub](https://github.com/Mazen-Aboulkhair/mazen.shaker/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### "const" Keyword 

-When a function is declared as const, it can be called on any type of object, const object as well as non-const objects.

-Whenever an object is declared as const, it needs to be initialized at the time of declaration. however, the object initialization while declaring is possible only with the help of constructors.

Following is a simple example of a const function:

```markdown
#include <iostream>
using namespace std;
 
class Test {
    int value;
 
public:
    Test(int v = 0) { value = v; }
 
    int getValue() const { return value; }
};
 
int main()
{
    Test t(20);
    cout << t.getValue();
    return 0;
}
```
Here the output will be:

```markdown
20
```
When a function is declared as const, it can be called on any type of object. Non-const functions can only be called by non-const objects. 

For example the following program has compiler errors:
```markdown
#include<iostream>
using namespace std;
 
class Test {
    int value;
public:
    Test(int v = 0) {value = v;}
    int getValue() {return value;}
};
 
int main() {
    const Test t;
    cout << t.getValue();
    return 0;
```

Here the output will be:

```markdown
passing 'const Test' as 'this' argument of 'int 
Test::getValue()' discards qualifiers
```



```markdown
Syntax highlighted code block

# Hi
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Mazen-Aboulkhair/mazen.shaker/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
