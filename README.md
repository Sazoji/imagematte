# Imagematte
idea for class-based segmentation/processing of raw photos and sequences, like a Cryptomatte
Using segmentation and a class list to digest a tiff/exr image (directly or thugh a denoised proxy) to a set of classes, which then can be set as IDs in a Cryptomatte. allowing for automatic sky separation; human, building, symbol, or object segmentation; directed denoising and processing of images; and a framework for inpainting and object removal within future deeplearning accelerated editing tools.

Basic Pipeline: raw images are demosaiced and could be tonemapped on ingest to linear, clips are cut for effects within the default ingest editor, then exported as a tiff, rgb exr file, or a png/jpeg. based on a premade list of classes to be edited or detected objects in a single image or example frame, segmentation is ran to produce a map for each image.
barring transperency and per-object tracking, these classes can make up the ID map of a cryptomatte and drive the digestion process, including a feathering zone or (depending on if the segmentation/detection does a pass for each class and detects multiple onbjects for the same pixel) a weaghted mixing of classes can be collected before digestion. each class id can than be masked and form a cryptomatte with each layer being a class in the object. these classes can than be used as layers or for image processing ideal/wanted for only certion parts of the image, while only requireing a paintdropper.
