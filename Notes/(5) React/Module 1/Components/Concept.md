Your next assignment as a developer is to add the details for the complete week, day-wise, to the webpage.

![[Pasted image 20231113140751.png|450]]
Each *detail-card* is the same just with different values and color. Coding it over and over again isn't the best way. 

A better approach would be to create one card and use it, over and over again, just like JavaScript **objects' instances**.

This is called **Component Architecture**, which forms the basis of React. 
React-apps are *built* using components, just like *Lego bricks*.

![[Pasted image 20231113134723.png|600]]

### Approach
Say a website contains a *header*, a *main-section* and a *footer*. Each of the section can be a Component.

![[Pasted image 20231114143834.png|300]]

In React, each component, conventionally, has its own [[JSX#^5b2a82|JSX]] file with **its name capitalized**.
Each of the file will contain the actual HTML element which will be displayed onto the webpage. 


![[Pasted image 20231116124508.png|450]]


The basic component called the **Root Component** gets created whenever a React app is created. All the components to be displayed on the webpage must be ***imported*** inside the **root component**.


![[Pasted image 20231116123852.png|600]]
