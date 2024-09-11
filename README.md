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
