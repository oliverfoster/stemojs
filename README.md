stemojs
=======

(Semi-Transparent) Evented Model Overlay - used for overlaying JSON models that require change/addition/removal events
  
  
##Basic Usage
```

var jsonModel = {
  o1: {
    o2 : {
      a1: [
        "i0",
        "i1",
        "i2"
      ]
    },
    o3: {
    
    }
  }
};

var stemoOverlay = new Stemo(jsonModel);


stemoOverlay.o1.o2.a1[0] == "i0"

stemoOverlay.o1.o2.a1.on("change", function( path, value, stemoNode, attributeName ) {

  alert("trigger");

});

stemoOverlay.o1.o2.a1[0] = "new value";




```
