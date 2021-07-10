# Global Attributes

class----------------Deﬁnes one or more class names for an element. See Classes and IDs.
contenteditable --Sets whether the content of an element can be edited.
contextmenu -----Deﬁnes a context menu shown when a user right-clicks an element.
dir -------------------Sets the text direction for text within an element.
draggable ---------Sets whether an element can be dragged.
hidden -------------Hides an element not currently in use on the page.
id --------------------Deﬁnes a unique identiﬁer for an element. See Classes and IDs.
lang----------------- Deﬁnes the language of an element's content and its text attribute values. See Content
Languages.
spellcheck ---------Sets whether to spell/grammar check the content of an element.
style -----------------Deﬁnes a set of inline CSS styles for an element.
tabindex ------------Sets the order in which elements on a page are navigated by the tab keyboard shortcut.
title ------------------Deﬁnes additional information about an element, generally in the form of tooltip text on
mouseover.
translate -----------Deﬁnes whether to translate the content of an element.

## Contenteditable Attribute

**<p contenteditable>This is an editable paragraph.</p>**
Upon clicking on the paragraph, the content of it can be edited similar to an input text ﬁeld.
When the contenteditable attribute is not set on an element, the element will inherit it from its parent. So all child
text of a content editable element will also be editable, but you can turn it oﬀ for speciﬁc text, like so:'

Upon clicking on the paragraph, the content of it can be edited similar to an input text ﬁeld.
When the contenteditable attribute is not set on an element, the element will inherit it from its parent. So all child
text of a content editable element will also be editable, but you can turn it oﬀ for speciﬁc text, like so:

![image-20210630161552965](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630161552965.png)

```html
    <!DOCTYPE html>
    <html lang = "en">
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <p contenteditable>
                This is an editable paragraph.
                <span contenteditable="false">But not this.</span>
            </p>
        </body>
    </html>
```

