# About Me

TODO

![cool UI]( images/subscript-ipad.jpg )

# Current Projects

## [WebCompiler](https://github.com/SuperSwiftDev/WebCompiler)

Static Site Compiler (as opposed to a SSG) with an emphasis on simplicity, robustness, component based reusability, and with an eye for producing optimized static content in terms of machine legibility.

All file paths are relative, you can include files with relative paths and the compiler normalizes everything relative to the output directory at compile time. You can include files and pass in content, the included files can transform the passed in HTML AST via macro tags like enumerate, to turn a fragment to a tab view, and whatnot… Very useful. I can talk it more if anyone is interested. As an amateur compiler engineer I’d love for this to be used in the real world. Plus, nowadays machine legibility matters more than ever and especially because Google bot is no longer the primary concern so you may as well keep the site, content and metadata suitable for the lowest common denominator client, which nowadays are machines
(the age of AI assistants that search and gather information on the user's behalf, all of which generally don't use google).

```html
<!-- pages/index.html -->
<include src="../common/main.html">
    <h1>Hello World</h1>
</include>

<!-- common/main.html -->
<include src="header.html"></include>
<main>
    <content></content>
</main>
<include src="footer.html"></include>
```

## [WebAutomation](https://github.com/SuperSwiftDev/WebAutomation)

Working on a new DSL, a rewrite of the basic implementation from [WebCompiler](https://github.com/SuperSwiftDev/WebCompiler).

### Background 

I've built complex pipelines that composed LLMs for generating 'publication quality' datasets. 

Here is an example, for generating dictionary datasets.

```liquid
<prompt name="process">
<message role="system">
{% if errors.size > 2 %}
You will fix all JSON syntax errors, JSON schema model validation errors, and then compile the corrected JSON dataset.
{% else %}
{{ system_message }}
{% endif %}
</message>
<message role="user">{{ instructions }}</message>
{% for error in errors %}
<message role="assistant">{{ error.response }}</message>
<message role="user">
{{ error.message }}
There is an issue with your compiled JSON object!
</message>
{% endfor %}
{% if errors.size > 0 %}
<message role="system">
Follow these instructions:
1. Take heed of the following schema:

{{json_schema}}

2. The task remains: populate the requested JSON object following the provided schema and then return the compiled data.

Hint: we do not want the schema but the data the schema represents.
</message>
{% endif %}
</prompt>
```

The goal here is to generalize the core ideas I've learned into a reusable, general purpose format. 


### Tentative DSL

```html
<schema src="./schema-1.json" id="schema-1"></schema>

<prompt name="fix-json-object" input:schema="of type Schema" input:json-value="of type String">
    <set response-format="json-object"></set>
    <msg role="system">
        <p>You previously returned invalid JSON that does not conform to the expected schema.</p>
        <p>Your task is to fix the syntax and ensure the structure matches the schema exactly.</p>
        <p>⚠️ Only return the **corrected JSON data** — do not include the schema, explanation, or any additional text.</p>
    </msg>
    <msg role="user">
        <p>Here is the malformed JSON:</p>
        <p from="json-value" format="pretty"></p>
    </msg>

    <msg role="user">
        <p>Here is the expected JSON schema:</p>
        <p from="schema" format="pretty"></p>
    </msg>
</prompt>



<prompt name="generate-user-profile" input:schema="of type Schema" input:json-value="of type String">
    <set response-format="json-object"></set>
    
    <msg role="system">
        <p>You are a strict JSON generator. Only return a JSON object conforming to the schema below.</p>
    </msg>

    <msg role="user">
        <p>Create a user profile for a new user named Sarah. Include her name, age, and whether she is a
        premium member.</p>
    </msg>

    <msg role="user">
        <p>Here is the JSON schema:</p>
        <p from="schema" format="pretty"></p>
    </msg>

    <breakpoint
        type="msg"
        role="assistant"
        verification="schema">
    </breakpoint>
</prompt>
```

Notes: 
- How should I accommodate validation loops? E.g.,
  > ```liquid
  > {% for error in errors %}
  > <message role="assistant">{{ error.response }}</message>
  > <message role="user">
  > {{ error.message }}
  > There is an issue with your compiled JSON object!
  > </message>
  > {% endfor %}
  > ```

## Other Projects

- [Native iOS Markdown Rendering](https://github.com/SuperSwiftMarkup/SuperSwiftMarkdownPrototype)
- ChatBot App with a branching conversational data model.
- Will be working on a rewrite of the app that compiled my [freeform chemistry notes](https://colbyn.github.io/old-school-chem-notes/dev/chemistry-1010---fall-2021/week-14-acids-and-bases.html). 





# Links

- [My Beautiful Math Notes](https://colbyn.github.io/school-notes-spring-2020/): Looks best on wide viewports.
- [My Experimental Chemistry Notes](https://colbyn.github.io/old-school-chem-notes/dev/chemistry-1010---fall-2021/index.html): from the root table of contents, click on any option to see my freeform notes.
- [The Tao Te Ching](https://colbyn.github.io/tao-te-ching-book/)

## Contact

- Email: hello@colbyn.com
