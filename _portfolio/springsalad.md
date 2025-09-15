---
caption: #what displays in the portfolio grid:
  title: Molecular Analysis and Visualization
  subtitle: Research Project
  thumbnail: assets\img\portfolio\springsalad_thumbnail.PNG
  
#what displays when the item is clicked:
title: Molecular Analysis and Visualization
type: video
video_url: https://www.youtube.com/embed/fprTymjZa5w?si=6muePOadoz2NldNV
subtitle: Research Project for UConn Health

---
The goal of this project was to create a Python package that could analyze and visualize the results of [SpringSaLaD](https://vcell.org/ssalad) simulations. SpringSaLaD is a spatial simulation tool that accounts for the three dimensional structure when considering interactions between molecules. These molecules are allowed to bond with each other according to certain rules specified by the user. The result is that large clusters have the potential of forming over the course of the simulation. SpringSaLaD currently outputs the results for these clusters in several CSV files. However, these are difficult to interpret on their own, especially if there is a large amount of data. To address this, the simulation data was converted into a format that could be understood by visualizations that were developed for a non-spatial simulator ([MolClustPy](https://molclustpy.github.io/index)). Additionally, analysis was done on the existing data to calculate more cluster properties and visualize them as well. Finally, a SpringSaLaD executable was included in the program so that users are able to run and modify simulations without using the SpringSaLaD GUI. In addition to publishing this code as a Python package, two Jupyter Notebooks were made that serve as the documentation and tutorial for the package. One of the main challenges for this project was reading and modifying a large amount of code written by someone else to apply it to a new problem.

{:.list-inline}

- Website: [SpringSaLaDpy](https://springsaladpy.github.io)
- Research Paper: [BPS2025 - SpringSaLaDpy](https://www.cell.com/biophysj/abstract/S0006-3495(24)03414-3)
- GitHub Repository: [SpringSaLaDpy Demo](https://github.com/SpringSaLaDpy/SpringSaLaDpy_demo)