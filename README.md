# Graphical Enhancements for Effective Exemplar Identification in Contextual Data Visualizations

> An exemplar is an entity that represents a desirable instance in a multi-attribute configuration space. It offers certain strengths in some of its attributes without unduly compromising the strengths in other attributes. Exemplars are frequently sought after in real life applications, such as systems engineering, investment banking, drug advisory, product marketing and many others. We study a specific method for the visualization of multi-attribute configuration spaces, the Data Context Map (DCM), for its capacity in enabling users to identify proper exemplars. The DCM produces a 2D embedding where users can view the data objects in the context of the data attributes. We ask whether certain graphical enhancements can aid users to gain a better understanding of the attribute-wise tradeoffs and so select better exemplar sets. We conducted several user studies for three different graphical designs, namely iso-contour, value-shaded topographic rendering and terrain topographic rendering, and compare these with a baseline DCM display. As a benchmark we use an exemplar set generated via Pareto optimization which has similar goals but unlike humans can operate in the native high-dimensional data space. Our study finds that the two topographic maps are statistically superior to both the iso-contour and the DCM baseline display.

## Branches

This is an open source tool for CDV graphical enhancements. The repo includes four branches, each of which represents a graphical enhancement:

- main: the basic data context map[[1]](#1) layout working as a baseline
- iso-contour: the iso-contour design from data context map that visualizes constraints by colored areas
- value-shaded: the value-shaded design that visualizes constraints by progressively fading colors and blended shapes
- terrain: the 2.5 terrain design that visualizes the dataset as a geographic map with a fixed viewing angle.


## Installation

This project uses `ASP.NET Core`, `JavaScrip` and `C#` for development. To fully set up a project with `ASP.NET Core`, please see the reference [here](https://docs.microsoft.com/en-us/aspnet/core/tutorials/razor-pages/razor-pages-start).

- .NET SDK 3.1.414
- .NET runtimes:
  - Microsoft.AspNetCore.App 3.1.20
  - Microsoft.NETCore.App 3.1.20

You may use Visual Studio to run the project

## Project Structure

### ./Pages

  - `DCM.cshtml` has the front end code for the page
  - `DCM.cshtml.cs` has the corresponding back end code for file receiving and data processing

### ./wwwroot

  - This folder has corresponding `javascript`, `css` files and libs that are used for front end rendering

### ./DataProcess.cs
  - The implementation of data context map

## User Study Analysis

All the user study data, testing datasets and evaluation scores are stored under `./user-study-data`. User study data is stored in `.csv` files under each graphical design folder and user subfolder. Each `.csv` file keeps the index and names of a data object that a user chose in each dataset. 

### Subfolders
  - `./baseline` has 8 users that did user study on the baseline data context map. Each subfolder under `./baseline` contains data collected from a user on 4 datasets, they are stored in each individual `.csv` files
  - `./iso-contour` has 8 users that did user study on iso-contour map
  - `./value-shaded` has 8 users that did user study on value-shaded map
  - `./terrain` has 8 users that did user study on terrain map
  
### Files
  - `car.csv`, `univ.csv`, `wine.csv` and `pokemon.csv` are testing datasets
  - `scores.xlsx` has all the scores that evaluate users' choices. The formula to calculate scores can be found in our [paper](https://ieeexplore.ieee.org/abstract/document/9765327)

## References

<a id="1">[1]</a> 
Cheng S, Mueller K. The data context map: Fusing data and attributes into a unified display[J]. IEEE transactions on visualization and computer graphics, 2015, 22(1): 121-130.

## Citation
```
@article{zhang2022graphical,
  title={Graphical Enhancements for Effective Exemplar Identification in Contextual Data Visualizations},
  author={Zhang, Xinyu and Cheng, Shenghui and Mueller, Klaus},
  journal={IEEE Transactions on Visualization and Computer Graphics},
  year={2022},
  publisher={IEEE}
}
```
