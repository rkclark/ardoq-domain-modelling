Guide to Domain Modelling in Ardoq
-----

### What is Ardoq?

[Ardoq](https://ardoq.com/) is an information modelling tool which can be used to model and visualise basically anything - but its strengths are modelling inter-related or hierarchical information.

It is free for individuals and small teams!

### Why Use It?

Ardoq lets you quickly input and edit the objects and messages that exist in your domain model, making changes and re-design super straightforward. As soon as you make changes to your objects, these are reflected in the auto-generated Sequence Diagram visualisation.

You can invite others to collaborate on your model, and download your sequence diagram as an image to include in other documentation.

It also offers a comprehensive API and the ability to create your own, custom visualisations in Javascript!

### Getting Started

Go ahead and make an account at [ardoq.com](https://ardoq.com/). You can sign in with Github which is awesome.

Whenever you start a new project in Ardoq you will start by creating a new workspace to work in. Each workspace is based on a "model", and it is the model that determines what you can create in the workspace. For example, an "IT Infrastructure" model might let you create servers, networks and locations and the relevant relationships between them.

You are going to need a new workspace model template for your domain model, one that lets you create objects (and maybe a user!).

### Creating a Domain Model template

> Quick point on language. Ardoq refers to your "things" (i.e. Objects) as "Components". It refers to the relationships between your things as "References".

- From the Dashboard, click 'ADD NEW' next to Workspaces.
- Give your workspace a name, i.e. the name of your project.
![Name workspace](https://github.com/rkclark/ardoq-domain-modelling/blob/master/img/name_workspace.png)
- Scroll down and you will see the available workspace templates. We need to make our own, so scroll down to the bottom and select Blank Workspace.
![Blank workspace](https://github.com/rkclark/ardoq-domain-modelling/blob/master/img/blank_workspace.png)

#### Creating Components

You will now be presented with the Model Editor, where we can start setting up our workspace template.

The first screen deals with creating our component types. Change the options on the blank component type to make it our Object component, like this:

![Create Object](https://github.com/rkclark/ardoq-domain-modelling/blob/master/img/create_object.png)
