import qupath.lib.gui.tools.MeasurementExporter 
import qupath.lib.objects.PathAnnotationObject

//Select manual annotation of interest
selectAnnotations()
//Segment red thresholded areas
createAnnotationsFromPixelClassifier("modelRed", 100.0, 1.0E17, "SPLIT")
//Store original red objects
original_red = getAnnotationObjects()
//Select positive red objects
selectObjectsByClassification("positive_red")
//Store positive red objects
original_red = getSelectedObjects()
//Dilate postive red objects
runPlugin('qupath.lib.plugins.objects.DilateAnnotationPlugin', '{"radiusMicrons":5.0,"lineCap":"ROUND","removeInterior":false,"constrainToParent":false}')
//Delete original red objects
removeObjects(original_red,true)
//Select positive red objects to measure
selectObjectsByClassification("positive_red")
selectedDilated = getSelectedObjects()
//Measure dilated red objects on red and green channel
addPixelClassifierMeasurements("modelRed", "modelRed")
addPixelClassifierMeasurements("modelGreen", "modelGreen")

//Select current project
def project = getProject()
//Store images per project
def imagesToExport = project.getImageList()

// Separate each measurement value in the output file with a tab ("\t")
def separator = "\t"

// Choose the columns that will be included in the export
// Note: if 'columnsToInclude' is empty, all columns will be included
def columnsToInclude = new String[]{"modelGreen: positive_green area µm^2","modelRed: positive_red area µm^2", "Image", "Object ID", "Name", "Class"}

// Choose the type of objects that the export will process
// Other possibilities include:
//    1. PathAnnotationObject
//    2. PathDetectionObject
//    3. PathRootObject
// Note: import statements should then be modified accordingly
def exportType = PathAnnotationObject.class

// Choose your *full* output path (note that slashes need to be in this position= //////)
def outputPath = "C:/Users/acayuela/Desktop/results.csv"
def outputFile = new File(outputPath)

// Create the measurementExporter and start the export
def exporter  = new MeasurementExporter()
                  .imageList(imagesToExport)            // Images from which measurements will be exported
                  .separator(separator)                 // Character that separates values
                  .includeOnlyColumns(columnsToInclude) // Columns are case-sensitive
                  .exportType(exportType)               // Type of objects to export
                  //.filter(obj -> obj.getPathClass() == getPathClass("Tumor"))    // Keep only objects with class 'Tumor'
                  .exportMeasurements(outputFile)        // Start the export process

print "Done!"
