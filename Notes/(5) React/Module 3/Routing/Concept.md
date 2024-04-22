[[SPA]] or Single Page Applications are an efficient way of making websites. Simply put, the browser, instead of loading complete HTML files, loads only the components needed. 

### Approach
Say, a website has 3 webpages, `Home`, `Services` and `About`. 


![[Pasted image 20231119213527.png]]



If this website is to be constructed as an SPA, each of the webpages will have its own React component. Whenever the user visits another webpage, only the component that changes will be rendered.


![[Pasted image 20231119193832.png|250]]



To achieve this, instead of using the anchor tag, `<a>`, a similar React component is used to link the webpages with the items of the ***Navbar*** or **Navigation Bar** called `Link`.



![[Pasted image 20231119213629.png|600]]


