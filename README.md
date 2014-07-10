Advanced 3D Seismic Visualization in Python
==========================================

Data and ipython notebook for my talk at Scipy2014.

Abstract
--------

3D reflection seismic data acquired [offshore of southeast Japan](http://penecontemporaneo.us/scipy2014/LocationMap.png "Location Map") as part of the Nankai Trough Seismogenic Zone Experiment  (NanTroSEIZE) provides a unique opportunity to study active accretionary prism processes.  The 3D seismic volume revealed complex interactions between active sedimentation and tectonics within [multiple slope basins](http://penecontemporaneo.us/scipy2014/inline_2695_w_interp_brown_seismic.png "Cross section through entire accretionary prism illustrating multiple isolated sedimentary basins") above the accretionary prism. However, our ability to understand these interactions was hindered without access to expensive specialized software packages. 

We implemented stratal slicing of the 3D volume and co-rendering of multiple attributes in python to better visualize our results.  Stratal slicing allows volumetric attributes to be displayed [in map view along an arbitrary geologic timeline](http://penecontemporaneo.us/scipy2014/stratal_slicing_animation.gif "Stratal Slicing Animation")(~30MB animated gif) by interpolating between interpreted geologic surfaces.  This enhances the visibility of subtle changes in stratigraphic architecture through time. Co-rendering coherence on top of seismic amplitudes facilitates fault interpretation in both cross section and map view.  This technique allowed us to [confidently interpret faults](http://penecontemporaneo.us/scipy2014/ContemporaneousStrikeSlipAndNormalFaults.png "Corendering attributes for fault interpretation") near the limit of seismic resolution.  

The scientific python ecosystem proved to be an effective platform both for making publication-quality cross sections and for rapidly implementing state-of-the-art seismic visualization techniques. We created [publication quality cross sections](http://penecontemporaneo.us/scipy2014/Basin_uplift.png "Example cross section") (some annotations added in Inkscape) and interactive 2D visualizations in ``matplotlib``.  For 3D display of seismic volumes we used ``mayavi`` to easily create interactive scenes. ``scipy.ndimage`` provided most of the underlying image processing capability and allowed us to preform memory-efficient operations on >10GB arrays.  

