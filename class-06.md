# Reading Notes
### class 06


## Understanding the Problem Domain

- Writing code is a lot like putting together a jigsaw puzzle.  We put together code with the purpose of building components that we have taken out of the “bigger picture” of the problem domain.

- It is very difficult to solve a problem before you know the question.

- You can often make the problem domain easier by cutting out cases and narrowing your focus to a particular part of the problem.

- make sure you understand a problem inside and out before you try and solve it with code

## Object Literals

- Objects group together as set of variables and functions to create a model of something youi would recognize from the the real world.

- In an object, variables and functions take on new names.

- Like variables and named functions, properties and methods have a name and a value. 

- In an object, that name is called a key.

- An object cannot have two keys with the same name.

```updateInfo.push = ({
      fname: encodeURIComponent(toTitleCase($("#FName").val())),
      lname: encodeURIComponent(toTitleCase($("#LName").val())),
      address1: encodeURIComponent(toTitleCase($("#address1").val())),
      address2: encodeURIComponent(toTitleCase($("#address2").val())),
      city: encodeURIComponent(toTitleCase($("#city").val())),
      state: encodeURIComponent($("#state").val()),
      zip: encodeURIComponent($("#zip").val()),
      email: encodeURIComponent($("#email").val()),
      phone: encodeURIComponent($("#phone").val())
}); 
```

- You access the properties or methods of an object using dot notation. 

- You can also access properties using square brackets.

``` var person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
```

## Document Object Model (DOM)

- The browser represents the page using a DOM tree.

- ![DOM](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/DOM-model.svg/1200px-DOM-model.svg.png)

- Dom tress have four types of nodes: document nodes, element nodes, attribute nodes, and text nodes.

- You can select element nodes by their id or class attributes, by tag name, or using CSS selector syntax

- Whenever a DOM query can return more than one node, it will always return a NodeList.

- Al element node can contain multiple text nodes and child elements that are siblings of each other.

- ![Dom element nodes](https://1.bp.blogspot.com/-XVMcn0CI6zQ/XEH1WliVqoI/AAAAAAAAAS8/gYzL50SaBsU_VS09nm8e842PhKEh7UYyQCLcBGAs/s1600/DOM%2BSTRUCTURE.png)

- Bowsers offer tools for viewing the DOM tree
