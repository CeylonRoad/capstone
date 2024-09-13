# Github
1.	Create a Github repository
2.	CD to the app directory
3.	Type git init
4.	Type git add .
5.	Type git commit -m “first commit”
6.	Type git remote add origin https://github.com/ceylonroad/your-repository-name.git
7.	Type git branch -M main
8.	Type git push -u origin main
### If there is any changes to the code then proceed the next step
1.	git add .
2.	git commit -m “second commit”
3.	git push origin main

# Single JS file Import
```
    React.useEffect(() => {
        const LoadExternalScript = () => {
            const externalScript = document.createElement("script");
            externalScript.id = "external";
            externalScript.async = true;
            externalScript.type = "text/javascript";
            externalScript.setAttribute("crossorigin", "anonymous");
            document.body.appendChild(externalScript);
            externalScript.src = './assets/js/main.js';
      };
      LoadExternalScript();     
      
        return () => {      
      
        };
      }, []);

```
# ------------------------------------------------------------------------
# Multiple JS file Import

```
  useEffect(() => {
    // let scripts = [
    //   { src: "assets/vendor/bootstrap/js/bootstrap.bundle.min.js" },
    //   { src: "assets/vendor/aos/aos.js" },
    //   { src: "assets/vendor/glightbox/js/glightbox.min.js" },
    //   { src: "assets/vendor/purecounter/purecounter_vanilla.js" },
    //   { src: "assets/vendor/imagesloaded/imagesloaded.pkgd.min.js" },
    //   { src: "assets/vendor/isotope-layout/isotope.pkgd.min.js" },
    //   { src: "assets/vendor/swiper/swiper-bundle.min.js" },
    //   { src: "assets/js/main.js" }
    // ]
    const LoadExternalScript = (e) => {

      // scripts.map(item => {
      //   const script = document.createElement("script")
      //   script.id = "external"
      //   script.src = item.src
      //   script.async = true
      //   script.defer = false
      //   script.type =  "text/javascript"
      //   document.body.appendChild(script)
      // })
    
      const externalScript = document.createElement("script");
      externalScript.id = "external";
      externalScript.async = false;
      externalScript.type = "text/javascript";
      externalScript.setAttribute("crossorigin", "anonymous");
      externalScript.src = 'assets/js/main.js';
      document.body.appendChild(externalScript);
 
    };

```

#---------------------------------------------------------------------------------
# Using Helmet

```
//Method 1
import React from "react";
import "./App.css";
import { Helmet } from "react-helmet";

function App() {
    return (
        <div className="App">
            <h1>
              Hello World
            </h1>
            <Helmet>
               <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
            </Helmet>
        </div>
    );
}

export default App;

```
#---------------------------------------------------------------------------------
# Install AOS Package

```
npm i aos — save

import AOS from "aos";
import "aos/dist/aos.css";

useEffect(() => {
    AOS.init();
    AOS.refresh();
  }, []);
  
```
