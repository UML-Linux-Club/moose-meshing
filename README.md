# COREFORM-CUBIT Information

The [Coreform-Cubit](https://coreform.com/products/downloads/) Coreform-cubit is a meshing software, which will be used for creating custom geometry and meshes.
Here we collect information for installation of Coreform-Cubit on typical systems for members of the UML Linux Club.

<span style="color:red"><b>A [course on ODE/PDEs, Engy-5310 Computational Continuum Transport Phenomena (Nuclear Energy)
](https://github.com/dpploy/engy-5310) at UMass Lowell, Dept. of Chemical Engineering, Nuclear Energy Program, is in development where the notes and homework could be used during club meetings on this topic: MOOSE.<b></span>

# Table of Contents<a id="toc">
+ [Installation of Coreform-Cubit](#Coreform-Cubit)
+ [Create a Rectangle](#geometry)
+ [Create Side Sets](#sidesets)
+ [Create Mesh](#mesh)

## [Installation of Coreform-Cubit](#toc)<a id="Coreform-Cubit"></a>
1. Proceed to the following website and install respected .exe file
 + [Coreform-Cubit](https://coreform.com/products/downloads/) 
2. Run the program 
3. It will ask for the key
 + `cubit-learn`
4. Restart program
    

## [ Create a Rectangle](#toc)<a id="#geometry"></a>
    
Let us create a simple 2-d Rectangle

1. Create new file
2. Right hand side; under `Command Panel` drop down box
3. Select the Mode `Geometry mode` (blue shapes icon)
4. Select the Entity `Surface`
5. Select the Action `Create Surface`
6. Specifiy y = 5 and x =5 
7. Select z-plane 
    
## [ Create Side Sets](#toc)<a id="#sidesets"></a>
    
 Let us create side sets, aka boundary vertices, for declaration in MOOSE input file

1. Select the Mode`Analysis Groups and Materials` (orange block icon)
2. Select the Entitiy `Sideset`
3. Select the Action `Create Sideset`
4. Create a Side set ID (Equivalent to the curve id)
5. Create a Side set name (Equivalent to the boundary label i.e outlet)
6. Select `Curve`
7. To see the Curve ID's and location go to the left side select the drop down of the `Sheet Bodies` tab
8. Drop down the `Surface` tab
9. Line up the boundary name of interest to the curve id and Side set name
i.e inlet is curve 6 

## [ Create Mesh](#toc)<a id="#mesh"></a> 
1. Select the Mode`Mesh` (orange block icon)
2. Select the Entitiy `Surface`
3. Select the Action `Intervals`
4. Select `Automatic Sizing`
    + note this is the most basic of all meshes (QUAD9)
5. Where it says surface ID select your surface
6. Press `Mesh`
