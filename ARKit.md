Pipeline:
    1. Prepare Resource
        detect 2D image
            new AR Resource Group
            drag and drop picture
        show 3D Image 
        video.mp4

    2. setup configuration
        (1) ARWorldTrackingConfiguration
        (2) ARImageTrackingConfiguration
                get configuration by ARImageTrackingConfiguration()
                load the image needed to detect to trackToimage
                setup trackToimage to configuration 

    3. create and configure nodes for anchors added to the view's session
        (1) create node and return node
        (2) downcast anchor to ARImageAnchor 
        (3) create SCNPlane and setup material (showScene, Image, Color)
        (4) create planeNode and rotate the plane
        (5) add planeNode to node by addChildNode() method
        (6) create showNode and load resource to the node
            seleect different resource by imageAnchor.referenceImage.name
        (7) create showScene and setup attributes
        (8) add showNode to showScene
        (7) add the showNode to planeNode
