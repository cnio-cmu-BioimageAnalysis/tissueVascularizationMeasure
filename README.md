# tissueVascularizationMeasure
This is a Groovy script to work within QuPath environment to identify vascular areas and measure them on different channels
## Download tissueVascularizationMeasure.groovy script
1. Go to the ``GitHub`` repository
2. Click on ``tissueVascularizationMeasure.groovy``>``Download raw file``
3. The repo will be found at ``Downloads`` directory.
## Running tissueVascularizationMeasure.groovy through Windows Command Line on a Single Image
``"QuPath-0.4.3 (console).exe" script "absolutePath/to/script.groovy" -i="absolutePath/to/image" ``
## Running tissueVascularizationMeasure.groovy through Windows Command Line on a Project
``"QuPath-0.4.3 (console).exe" script "absolutePath/to/script.groovy" -p="absolutePath/to/project.qpproj" ``
### Parameters Explanation:
-  ``script "path/to/script.groovy"`` : Apply the script to the specified image.
- ``-i,--image="absolutePath/to/image"`` : Apply the script to the specified image
- ``-p,--project="absolutePath/to/project.qpproj"``: Path to a project file (.qpproj)
## Running through QuPath GUI
1. Navigate to reach Script Editor tool:
   - By writing ``Show script editor`` on the search tool or by ``Automate``>``Show script editor``
     <p align="center">
    <img width="650" height="350" src="https://github.com/cnio-cmu-BioimageAnalysis/tissueVascularizationMeasure/assets/83207172/8ef809fd-36d4-4d2d-aa23-fcd9b1ab7f70">
    </p>
2. ``Show script editor`` tool will be displayed:
    <img width="650" height="350" src="https://github.com/cnio-cmu-BioimageAnalysis/tissueVascularizationMeasure/assets/83207172/c66c5637-dfd7-4ad5-9d79-84d231b523dc">
    </p>
   

2. Open the groovy script ``tissueVascularizationMeasure.groovy`` by  ``File``>``Open...``>``tissueVascularizationMeasure.groovy``
    <p align="center">
    <img width="500" height="350" src="https://github.com/cnio-cmu-BioimageAnalysis/tissueVascularizationMeasure/assets/83207172/f11ca21b-ac52-4876-a0ac-d4018369f4f7">
    </p>

3. Press ``Run`` button to compile the script.
