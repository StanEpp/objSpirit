## objSpirit

`objSpirit` is a wavefront obj loader written in C++14 and utilizing the **Spirit X3** library.

Spirit X3 Documentation [http://ciere.com/cppnow15/x3_docs/](http://ciere.com/cppnow15/x3_docs/ "Spirit X3 Documentation")

## Features
`objSpirit` supports some additional primitives and ight descriptors for easy definition of small scenes. Syntax:
```
sphere vertexIdx/radius
plane vertexIdx/normalIdx
pointLight posX/colorR/attenuation1 posY/colorG/attenuation2 posZ/colorB/attenuation3
directionalLight dirX/colorR/attenuation1 dirY/colorG/attenuation2 dirZ/colorB/attenuation3
```

## Further Notes
I developed `objSpirit` for use in several private projects and recently ported it to the new X3 version of spirit.
Spirit X3 is a heavy dependency but a very interesting, cool and crazy library. So I wanted to get my hands on it and `objSpirit` is the result.