Any file, such as a stylesheet, image or an icon,  used in a project is called an **asset**. 
By convention, these **assets** are to be stored in the `assets` folder inside the `src` folder.

### Accessing Assets
There are three ways to access and use assets in a React app.

* ##### Importing and Using, directly
Import the image and assign it a name using the `import..from` statements. Add in `logo` as the value of the `src` attribute.
  ```jsx
import logo from "./assets/logo.png";

<img 
	src={ logo }
>
  ```
<br>

* ##### Using `require`
Call the function `require` with file path as the argument wherever needed.
  ```jsx
<img
	src={ require("./assets/logo.png") }
>
  ```
<br>

* ##### Using an External URL 
Store the URL of an **external image**, *which is not locally downloaded on the system*, in a variable and use it wherever needed. 
  ```jsx
const logo = "https://www.example.com/images/logo.png";
<img 
	src={ logo }
>
  ```
<br>

### Using Assets
There are broadly two ways to use an asset in React.

* ##### Using the HTML elements
The conventional way of using assets using HTML tags such as, `<video>`, `<audio>` and `<img>`. <br><br>

* ##### Using Third-party Libraries
There are numerous libraries provided by other developers which can be installed *via* `npm` and looked [here](https://npmjs.org). For instance, `react-audio-player` and `react-video-player`.

  ```jsx
  import Audio from "react-audio-player";

  function App() {
	  const aud = "./assets/audio.mp3";
	   
	  return (
		  <Audio src={aud} />
	  );
  }
  ```
