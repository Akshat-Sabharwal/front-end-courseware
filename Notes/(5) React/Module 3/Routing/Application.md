To create a proper navigation system using ***routing***, another library, the `react-router-dom` which is paired along with `react`.

The approach to create the routing system can be broken down into steps.
<br>

* #### Creating the Components
The components, which essentially are distinct webpages, are created into separate files just like other React components.

  ```jsx
  // Home.jsx
  export function Home() {
  return (
	  <h1>This is the HomePage</h1>
  );
  }

  // Services.jsx
  export function Services() {
  return (
	  <h1>Know our Services</h1>
  );
  }

  // Contact.jsx
  export function Contact() {
  return (
	  <h1>Contact Us</h1>
  );
  }
  ```
  <br>


* #### Adding in the Routes
**Routes** are just like roadways. The road is, first, created and named. Only then, is it added to the official maps. This is the creation step.

  Routes are created using the `Route` and `Routes` components from the `react-router-dom` library. 

  ```jsx
  import { Route, Routes } from "react-router-dom";
  import Home from "./components/Home";
  import Services from "./components/Services";
  import Contact from "./components/Contact";

  export default function App() {
	  return (
		  <Routes>
			  // Create a Route to the URL, *the same one*, and webpage, Home 
			  <Route to="/" element={<Home />}>
			  
			  // Create a Route to the URL, /services, and webpage, Services 
			  <Route to="/servives" element={<Services />}>
			  
			  // Create a Route to the URL, /contact, and webpage, Contact
			  <Route to="/contact" element={<Contact />}>
		  </Routes>
	  );
  } 
  ```

  | Component | What it does |
  |--|--|
  | `Routes` | Used to group the individual `Routes` |
  | `Route` | Creates a URL for the webpage with the components to be rendered in it |

<br>


* #### Linking Webpages to Routes
This is done using the component `Link` from `react-router-dom`. It links the URL created above with the HTML elements of choice.

  ```jsx
  import { Link, Route, Routes } from "react-router-dom";
  import Home from "./components/Home";
  import Services from "./components/Services";
  import Contact from "./components/Contact";

  export default function App() {
	  return (
		  
		  // Create links to the URLs 
		  <Link to="/">Home</Link>
		  <Link to="/services">Services</Link> 
		  <Link to="/contacts">Contacts</Link>
		  
		  <Routes>
			  // Create a Route to the URL, *the same one*, and webpage, Home 
			  <Route to="/" element={<Home />} />
			  
			  // Create a Route to the URL, /services, and webpage, Services 
			  <Route to="/servives" element={<Services />} />
			  
			  // Create a Route to the URL, /contact, and webpage, Contact
			  <Route to="/contact" element={<Contact />} />
		  </Routes>
	  );
  } 
  ```