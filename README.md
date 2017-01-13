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

### Creating a Domain Model Template

> Quick point on language. Ardoq refers to your "things" (i.e. Objects) as "Components". It refers to the relationships between your things as "References".

- From the Dashboard, click 'ADD NEW' next to Workspaces.
- Give your workspace a name, i.e. the name of your project.

![Name workspace](https://github.com/rkclark/ardoq-domain-modelling/blob/master/img/name_workspace.png)

- Scroll down and you will see the available workspace templates. We need to make our own, so scroll down to the bottom and select Blank Workspace.

![Blank workspace](https://github.com/rkclark/ardoq-domain-modelling/blob/master/img/blank_workspace2.png)

### Creating Components

You will now be presented with the Model Editor, where we can start setting up our workspace template.

The first screen deals with creating our component types.

- Change the options on the blank component type to make it our Object component, like this:

![Create Object](https://github.com/rkclark/ardoq-domain-modelling/blob/master/img/create_object.png)

> Make sure you have opened Additional Properties and selected Return Value to be true!

- If you want to include a user in your domain model, click Add Top Level Component Type and setup another component, calling it User and giving it a different colour and icon.
- For User, don't bother selecting Return Value.

- Lastly, select to make your model flexible by selecting "ALLOW FLEXIBLE COMPONENT HIERARCHY". Don't worry about what this does, but trust me that it's a good thing.

![Make flexible](https://github.com/rkclark/ardoq-domain-modelling/blob/master/img/make_flexible.png)

### Creating References

- Click Next
- You are now on the screen that allows you to specify the reference types (i.e. relationships) for your model.
- By default you will see there is a "Depends on" reference type available. We want to create a Message type to link our Objects together.
- Click "Add new reference type", call it Message and change the colour and line style to whatever you like. You can always change it later.

![Make flexible](https://github.com/rkclark/ardoq-domain-modelling/blob/master/img/create_message.png)

> Note: If there is any custom data you want to save against your Objects or Messages, you can click Manage Fields at this point to set them up.

- The template is now ready. Click Save as Template and call it "Domain Model". Make sure to tick that it is a flexible hierarchy before you save. Next time you create a new workspace it will be available to use.
- After its saved as a template, click Save and our current workspace will now be using our model. Great!

### Making A Domain Model

*Note, this isn't an Ardoq user guide, so check out the help materials available in the app if you are new or want to learn the basics first!*

- If your workspace initialized with an example component (probably called Create Your Own Structure) then just delete it.
- Add new components for your objects (hint: click the blue +). Add a user component too if you want one. You'll now have something like this:

![Objects](https://github.com/rkclark/ardoq-domain-modelling/blob/master/img/objects.png)

- Link the objects together with messages. Mouse over an object and click on the link icon, then click on the object you want to create a reference to.
- On the menu that opens up, select the "Message" type and add the Return Value that you expect the target object to return. If there is no return value then just leave blank or put a placeholder like "[nothing]". The Order field determines the order of the message compared to other messages coming from that object. Just leave as 0 if you don't want to specify it.

![Refrence options](https://github.com/rkclark/ardoq-domain-modelling/blob/master/img/reference_options.png)

### Viewing the Sequence diagram

- The main ardoq window lists visualisations for you to select to view. Sequence Diagram should be available there. If not, click More and choose to Manage Views. Add the Sequence Diagram in the screen that opens up.

![Visualizations](https://github.com/rkclark/ardoq-domain-modelling/blob/master/img/visualizations.png)

- **Here's an example of the finished sequence digram!**

![Sequence diagram](https://github.com/rkclark/ardoq-domain-modelling/blob/master/img/sequence_diagram.png)

> Note, if you add a second reference between two components, you will need to refresh ardoq for it to appear in your sequence diagram.

You can make changes to the domain model within the sequence diagram itself, whether that is renaming/removing messages, changing message order or even adding new objects. Just play around with the options in the blue menu icon that appears when you hover over an object or a message :)

#### Taking It Further

You can model anything in Ardoq, creating custom workspace templates for any type of information you want to map. If your project has users and user stories, why not model them too? You could even create references between the user stories and the domain model. It's perfectly ok to create references between workspaces!

The standard Ardoq visualisations are good, but they won't always cater for every need. If you want to see your information represented differently, check out the Ardoq plugin editor. You can create your own visualisations using Javascript. Here are some examples that might help to get you started:

[Sunburst Diagram](https://github.com/rkclark/ardoq-sunburst-diagram)

[Multi Bar Chart](https://github.com/rkclark/ardoq-multi-bar-chart)
