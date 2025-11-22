# **3DCPolish**



### 3DC Polish - Add-on Documentation



3DC Polish is a Blender add-on designed to enhance and polish 3D meshes with simple deformation and remeshing tools. It provides intuitive controls for mesh refinement, noise-based detailing, and dynamic remeshing similar to ZBrush's DynaMesh functionality.

#### 

#### Compatibility





Blender Version: 4.3 and above



Operating Systems: Windows, macOS, Linux



Object Types: Mesh objects only





#### Installation





1. Download the 3dc\_polish.zip file
   
2. In Blender, go to Edit → Preferences → Add-ons
   
3. Click "Install" and select the downloaded file
   
4. Enable the add-on by checking the checkbox next to "Mesh: 3DC Polish"
   
5. Interface Location
   
6. The add-on panel is located in the 3D Viewport sidebar under the "3DC Polish" category (press N to open sidebar if hidden).



### 

### Features:



#### Edge Polish Section





* Refine mesh edges and enhance surface details



* Iterations: Number of times to repeat the polish operation (1-10)



* Details: Amount of surface details to preserve (0.0-1.0)



* Curvature Radius: Influence radius for polish operation (1-10)



* Edge Contrast: Intensity of edge highlighting (0.0-10.0)



* Polish Strength: Amount of polishing to apply (0.0-1.0)



* Curvature Threshold: Only affects sharper curvature areas at higher values (0.0-1.0)



* Blur: Post-processing smoothing iterations to get rid of artifacts (0-10)



* Usage: Click the "Polish" button to apply edge refinement based on your settings.



#### 

#### Deformation Section





* Real-time mesh deformation with preview



* Inflate: Inflate/deflate mesh along vertex normals (-2.0 to 2.0)



* Smooth: Smoothing iterations after deformation (0-100)



* Noise Type:



&nbsp;   Perlin: Smooth, natural-looking noise



&nbsp;   Fractal: Natural, terrain-like patterns



* Noise Strength: Intensity of noise displacement (0.0-1.0)



* Noise Scale: Frequency of noise pattern (0.0-1000.0)



* Noise Seed: Seed value for reproducible noise generation



* Real-time preview of deformations



* Randomize seed button for instant variation



* "Apply" button to commit changes and update base mesh







#### Dynamic Remesh Section





* Voxel-based remeshing with DynaMesh-like resolution control



* Resolution: Voxels across longest axis (64-2048)



* Warning: High resolutions (>256) may take exponentially longer to process



* Automatic voxel size calculation based on object bounds



* Automatic smoothing at high resolutions (512-2048)



* Volume-preserving remeshing



* Automatic shading smooth application





#### Workflow Examples





##### Basic Mesh Polish



* Select a mesh object



* Set Edge Polish parameters:



&nbsp;   Iterations: 1-3



&nbsp;   Details: 0.85



&nbsp;   Polish Strength: 0.7



* Click "Polish"





##### Surface Detailing



* Apply base mesh polish



* Use Deformation section:



&nbsp;   Set Noise Strength: 0.001-0.01



&nbsp;   Adjust Noise Scale for detail size



&nbsp;   Randomize seed until desired pattern



* Click "Apply"



##### 

##### High-Resolution Remeshing



* For sculpting preparation:



&nbsp;   Set Resolution: 512-1024



&nbsp;   Click "Remesh"



* The remesh tool preserves volume at all resolutions.







### 

### Performance Notes



* Edge Polish: Performance scales with CPU capability, mesh complexity and iteration count. Polishing speed on high polygon meshes is significantly slower.



* Comparison with Claypolish: Blender Python does not natively support GPU acceleration. Hence the performance takes a hit compared to zbrush's clay polish. 



* Remeshing: High resolutions (>512) significantly increase processing time. Voxel remeshing does not result in a good topology. It is the most useful for prototype/testing purposes



* Real-time Preview: Deformation preview updates instantly but may slow with dense meshes



* Limits: The add on does not have inbuilt safety limits. Extreme values can provide irregular results. Values close to defaults often produce the best results with simple increase in iterations!



* Artifacts: Use Blur slider to get rid of artifacts, if any, after polishing







### 

### Technical Details

#### 

#### Algorithms Used



* Curvature Detection: Local neighborhood curvature sampling for edge detection



* Noise Generation: Built-in Blender noise functions (Perlin, Fractal)



* Remeshing: Blender's voxel remesher with surface resolution mapping.



* Smoothing: Bmesh smoothing operations with boundary preservation





#### Data Management



* Creates temporary base mesh copies for deformation previews



* Automatically cleans up temporary data on unregister



* Non-destructive preview system for Deformation tools





### 

### Troubleshooting Common Issues





* Add-on not appearing: Ensure Blender version is 4.3+ and add-on is properly enabled



* No real-time preview: Check that a mesh object is selected and in Object Mode



* Remeshing fails: Ensure mesh is manifold and doesn't contain extreme non-manifold geometry







### 

### Best Practices



* Start with lower resolution meshes and gradually increase



* Polishing can be used as a clean up tool along with a finishing tool.



* Make use of the tools full capability by exploring edge contrast without polish for highlighting the edge curvature.



* Use moderate polish iterations (1-3) for balanced results



* Use Blur slider to get rid of any artifacts after polishing.



* Save work before applying high-resolution remeshing operations





###### Support: This add-on uses standard Blender APIs and should be stable across all supported platforms. For issues, ensure you're using the latest Blender version and that your system meets Blender's minimum requirements.


