---
- GuiCommand:/ru
   Name:FEM SolverCalculixCxxtools
   Name/ru:FEM Solver
   MenuLocation:Solve → Solver CalculiX Standard
   Workbenches:[FEM](FEM_Module/ru.md)
   Shortcut:
   SeeAlso:[FEM tutorial](FEM_tutorial/ru.md)
---


</div>

## Описание

[CalculiXccxTools](FEM_SolverCalculixCxxtools.md) enables usage of the [CalculiX](https://en.wikipedia.org/wiki/Calculix) solver. It may be used for:

1.  Setting analysis parameters
2.  Selecting working directory
3.  Running the CalculiX solver

## Использование

1.  <img alt="" src=images/FEM_SolverCalculixCxxtools.svg  style="width:24px;"> [FEM SolverCalculixCxxtools](FEM_SolverCalculixCxxtools.md) object is created automatically with creation of an **![](images/)_[Analysis_container](FEM_Analysis.md)**. Or use the following alternatives:
    -   Use **Solve → Solver CalculiX Standard**
    -   Press **S** then **X** shortcut keys




1.  Optionally set data properties of the **<img src="images/FEM_SolverCalculixCxxtools.svg" width=24px> CalculiXccxTools** object
2.  Double click on the **<img src="images/FEM_SolverCalculixCxxtools.svg" width=24px> CalculiXccxTools** object
3.  Select type of the analysis
4.  Click **Write .inp file**
5.  Click **Run CalculiX**

## Опции

By using **Edit .inp file** you can display and edit CalculiX input file manually before running analysis. In this case it might be useful to use parameter \"Split Input Writer = true\".

## Свойства

Default values can be set in the menu **Edit → Preferences → FEM → CalculiX**

-    **Analysis Type**:

    -   static
    -   frequency
    -   thermomech - for mechanical and thermal loads
    -   check - to check only the mesh <small>(v0.19)</small> 

-    **Beam Shell Result Output 3D**: note that CalculiX internally expands 1D and 2D elements into 3D elements to accomplish FE analysis

    -   false - results of 1D and 2D elements will be averaged to the nodes of original 1D or 2D mesh (i.e. purely bended beam will show 0 nodal stresses due to averaging)
    -   true - resulting mesh will contain 1D and 2D elements expanded to 3D elements

-    **Eigenmode High Limit**: Eigenvalues above this limit will not be calculated; **Note**: if eigenvalues of the model are above the high limit, CalculiX will finish without output

-    **Eigenmode Low Limit**: Eigenvalues below this limit will not be calculated

-    **Eigenmodes Count**: number of lowest eigenmodes to be calculated

-    **Geometric Nonlinearity**:

    -   linear - linear analysis will be performed if model does not contain nonlinear material
    -   nonlinear - nonlinear analysis will be performed

-    **Iterations Control parameter Cutb**: defines the second line of [CalculiX\' advanced iteration parameters](http://www.dhondt.de/ccx_2.17.pdf#subsection.8.24). Used if **Iterations Control Parameter Time Use** is set to *true*.

-    **Iterations Control Parameter Iter**: defines the first line of [CalculiX\' advanced iteration parameters](http://www.dhondt.de/ccx_2.17.pdf#subsection.8.24). Used if **Iterations Control Parameter Time Use** is set to *true*.

-    **Iterations Control Parameter Time Use**-   true - activates **Iterations Control parameter Cutb** and **Iterations Control Parameter Iter**
    -   false

-    **Iterations Thermo Mech Maximum**: maximum number of increments in thermomechanical analysis after which the job will be stopped.

-    **Iterations User Defined Incrementations**:

    -   true - automatic incrementation control will be switched off by DIRECT parameter
    -   false - incrementation control will be automatic

-    **Iterations User Defined Time Step Length**:

    -   true - activates **Time End** and **Time Initial Step** parameters
    -   false

-    **Material Nonlinearity**:

    -   linear - only linear material properties will be included in the analysis
    -   nonlinear - nonlinear material properties will be used from **<img src="images/FEM_MaterialMechanicalNonlinear.svg" width=24px> '''[Nonlinear mechanical material](FEM_MaterialMechanicalNonlinear.md)'''** object

-    **Matrix Solver Type**: type of the solver to solve equation system inside FE analysis. It may significantly affect calculation speed and memory demands. Suitability depends on your FE model and available hardware

    -   default - automatically selects matrix solver depending on available solvers (probably it will be Spooles)
    -   spooles - direct solver with support of multiple CPUs. Number of CPUs need to be set in **Edit → Preferences → FEM → CalculiX → Solver defaults → Number of CPU's to use**.
    -   iterativescaling - iterative solver with least memory demands, suitable if model contains mostly 3D elements
    -   iterativecholesky - iterative solver with preconditioning with and with low memory demands, suitable if model contains mostly 3D elements

-    **Split Input Writer**:

    -   false - write whole input into one \*.inp file to be used by CalculiX solver
    -   true - split solver inputs into more \*.inp files, that can clarify hand editing

-    **Thermo Mechanical Steady State**:

    -   true - steady state thermo mechanical analysis
    -   false - transient thermo mechanical analysis

-    **Time End**: time period of the step, used when parameter **Iterations User Defined Incrementations** or **Iterations User Defined Time Step Length** is *true*

-    **Time Initial Step**: initial time increment of the step, used when parameter **Iterations User Defined Incrementations** or **Iterations User Defined Time Step Length** is *true*

-    **Working Dir**: path to the working directory which will be used for CalculiX analysis files.

## Ограничения

When running a CalculiX, you might end up with **error 4294977295**. This means you don\'t have enough RAM space. You have then 2 options:

1.  reduce the number of mesh nodes, preferably by omitting geometry that is not absolutely necessary for your analysis
2.  buy more RAM for your PC

## Примечания

Original CalculiX documentation can be found at <http://dhondt.de/> in the \"ccx\" paragraph.

## Scripting


<div class="mw-translate-fuzzy">





</div>


{{FEM Tools navi

}} 