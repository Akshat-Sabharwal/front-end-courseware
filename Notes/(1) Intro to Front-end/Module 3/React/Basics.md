React is a JavaScript library developed by Meta to create UI components.

### Approach
React breaks down documents into components by making a **component hierarchy** each of which is reusable. Also, React solves the problem of frequent browser updates due to changes in the [[DOM]] by a process called **reconciliation**.

#### Reconciliation
React creates a virtual representation of the browser DOM in memory and compares it with the browser DOM to check for changes.

* A change in the document would first lead to a change in the virtual DOM of React 

* The updated version of the Dom will be compared with the previous version to identify the change.

* The change will then be made to the browser DOM

![[Pasted image 20230922231704.png|500]]

#### Component Hierarchy
Often, in web applications, elements *house* other elements. For instance, the shopping list below

![[Pasted image 20230922232626.png|500]]