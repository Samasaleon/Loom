Loom

Loom is a JavaScript library for creating and editing website and web application templates through a simple, chainable API.

Instead of manually editing a template's files and configuration, Loom lets you import a template as an object and modify it using JavaScript.

Status

Loom is currently in early development (v0.0.0).

The API and template format are experimental and may change.

Concept

Loom is built around a simple idea:

Template(blog)

does not create a template called blog.

Instead, it imports an existing blog.json template and returns it as a template object that can be edited.

For example:

Template(blog)
    .title("My Blog")
    .style({
        theme: "dark"
    });

To create a completely new template, Loom provides a blank template:

Template(new)
    .title("My Website");

The resulting template can then be configured using Loom's methods.

Basic Structure

A Loom project may contain templates such as:

templates/
├── blog.json
├── portfolio.json
└── landing-page.json

A template is represented by a JSON file containing the information Loom needs to construct the website or application.

A very simple template might look like:

{
    "name": "blog",
    "type": "website",
    "title": "My Blog",
    "style": {
        "theme": "light"
    }
}

The JSON format is intentionally simple during early development.

More properties and capabilities can be added as Loom develops.

API Philosophy

Loom is designed around method chaining.

A template can be progressively configured:

Template(blog)
    .title("My Blog")
    .style({
        theme: "dark"
    })
    .description("A personal blog");

The goal is for template configuration to read almost like a description of the project.

Templates

There are two basic ways to work with templates.

Import an existing template

Template(blog)

This loads the existing blog.json template.

Create a new template

Template(new)

This loads a blank template that can be configured from scratch.

Goals

Loom aims to provide:

A simple template representation

JSON-based templates

A chainable JavaScript API

Reusable website and web-app templates

Easy template customization

A clear separation between template data and the API used to modify it


Early Development

Loom is deliberately starting small.

The first versions will focus on establishing:

1. The template JSON structure


2. Template importing


3. Blank template creation


4. The Template() function


5. Basic template methods


6. Method chaining


7. Exporting the modified template



More advanced features should only be added once this foundation is stable.

Example

A future Loom workflow could look something like:

Template(blog)
    .title("My Personal Blog")
    .style({
        theme: "dark"
    })
    .author("John");

Loom would then use the resulting template object to produce the configured project.

License

License information will be added as the project develops.