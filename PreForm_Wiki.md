# Best Practices for Utilizing PreForm
#### Welcome Bourns Inc. Intern!
In this wiki, you will learn the best way to handle navigating the challenging world of SLA resin printing.

## What is SLA Printing?
"Stereolithography is a form of 3D printing technology used for creating models, prototypes, patterns, and production parts in a layer by layer fashion using photochemical processes by which light causes chemical monomers and oligomers to cross-link together to form polymers" - [Wikipedia](https://en.wikipedia.org/wiki/Stereolithography)

<img align="left" width="170" height="250" src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d6/Schematic_representation_of_Stereolithography.png/220px-Schematic_representation_of_Stereolithography.png">
  
Stereolithography: a light-emitting device a) A laser or DLP selectively illuminates the transparent bottom c) of a tank b) filled with a liquid photo-polymerizing resin. The solidified resin d) is progressively dragged up by a lifting platform e).

The main **advantage** of SLA printers is the very fine layer thickness (0.015 to 0.05 mm) compared to FDM (0.1 to 0.5 mm). As the image below shows the resolution of the SLA printing vs FDM. 

The main **disadvantage** of SLA printers are the material sensitivities and warpage due to the cleaning and curing process.

![image](https://manufactur3dmag.com/wp-content/uploads/2018/02/Above-3D-Printed-parts-made-in-FDM-SLA-SLS-technology-from-left-to-right-Image-Credit-Formlabs.jpg)

## How to Prepare to Export from Creo
#### At Bourns Inc. we use Creo as our flavor of CADing software (computer-aided design).
Once you've successfully finished CADing the part you wish to prototype, follow the steps below:
1. file -> save as -> save as copy
![image](https://github.com/C-Chicas/Bourns-Wiki/blob/main/Images/creo_1.png)
2. Save the file as an STL and choose **customize export**
![image](https://github.com/C-Chicas/Bourns-Wiki/blob/main/Images/creo_2.png)
3. Click **OK** and a menu will open. For **Chord Height** input **0** and Creo will automatically choose the smallest chord height. For **Angle Control** input **1**. Click **Apply**, if you see that the quality of your STL mesh is low **check** the box that says **Step Size** and input **a smaller number**. This will increase the quality (resolution) of your mesh/STL, otherwise click **OK**.
![image](https://github.com/C-Chicas/Bourns-Wiki/blob/main/Images/creo_4.png)

##### Congrats! You've successfully exported an STL with a high probability of it working well within PreForm!

## Using the From 3 on PreFrom
#### PreForm creates SLA printers for the consumer market and has an intuitive/easy to use software.
1. Launch **PreForm** (_If you do not have PreForm installed, download it from their official website and ask IT to install it for you._)
![image](https://github.com/C-Chicas/Bourns-Wiki/blob/main/Images/preform_1.png)
2. Click the **Name of the printer** on the top right of the image above. The page will change and here you can choose the **printer**, **resin**, and **layer thickness**. We usually use **Adaptive** for the layer thickness as the program decides how to vary the layer thickness depending on your model. Then check **Apply**.
![image](https://github.com/C-Chicas/Bourns-Wiki/blob/main/Images/preform_7.png)
3. Click **File** then **Open** and navigate to where your STL is saved to open it.
4. Once open, your STL will drop into the **built area** (_everything within the box_) and onto the **built plate** (_the surface with a grid_). **If prompted with a question about units, use the units the part was designed with**.
![image](https://github.com/C-Chicas/Bourns-Wiki/blob/main/Images/preform_2.png)
You'll see the program is mad with you, and it is. The parts enter the build area semi-randomly and need to placed correctly.
5. Using the **Orientation** tool, click **select base**
![image](https://github.com/C-Chicas/Bourns-Wiki/blob/main/Images/preform_3.png)
6. Your cursor will now be used to select the face that will be touching the build plate. In the example below, I chose the bottom flat face so that the part has the flattest side on the build plate. This is only for comfort sake as it's usually best practice to have a raft and supports prop up your part (which will be covered next).
![image](https://github.com/C-Chicas/Bourns-Wiki/blob/main/Images/preform_4.png)
7. Now that your part is in a more optimal printing position, navigate to the supports menu. When in the supports menu ensure that **Raft Thickness** under the **Advanced Settings** is set to **3.00 mm**. This has proven to consistently work.
![image](https://github.com/C-Chicas/Bourns-Wiki/blob/main/Images/preform_5.png)
8. Click **Auto Generate Selected** and PreForm will generate supports for the part/s selected.
![image](https://github.com/C-Chicas/Bourns-Wiki/blob/main/Images/preform_6.png)
9. Now, PreForm should be happy with you and all **PRINTABILITY** checks should appear green with a thumbs up. Click the orange button on the left toolbar and a menu will appear. If all looks right, click **Print Now** and the file will be sent to the Form 3.
![image](https://github.com/C-Chicas/Bourns-Wiki/blob/main/Images/preform_8.png)
10. Unless the printer has been **Primed** before hand (_Primed means that its waiting to print_), you will need to ready the printer for printing in the 3D printing room. The Form 3 will guide you through all the checks and necessary hardware on its display, then you're done!
