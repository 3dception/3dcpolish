 🟣 3DC Polish

As a 3D artist, I have worked in Blender for years and highly admired it's potential as the ultimate one‑stop shop for creators—modeling, texturing, animation, physics simulation all under one roof. However, when it comes to sculpting, I relied on ZBrush for its high‑fidelity, particularly its indispensable ClayPolish tool that effortlessly refined details and sharpened edges. But migrating fully to Blender meant leaving that polish behind... until now.

Introducing 3DC Polish! 

An add‑on born from my and the entire sculpting community's long‑standing call for a dedicated polishing solution. Since Blender's sculpting tools debuted, artists like us have dreamed of a native way to tighten surfaces, exaggerate creases, and add organic flair without jumping apps. I built this as a faithful Claypolish‑inspired substitute, optimized for Blender's ecosystem!


✨ Key Features: Polish, Deform, and Remesh with Precision

Edge Polish Mastery

    Iteratively sharpen curvature and creases while preserving fine details.

    Adjustable iterations, contrast, and thresholds for targeted edge enhancement—perfect for hard‑surface models or organic forms.

    Built‑in detail preservation for buttery‑smooth finishes.


Real‑Time Deformation Preview

    Inflate or deflate along vertex normals for volumetric tweaks.

    Layer on procedural noise (Perlin or Fractal) with customizable intensity, scale, and seed randomization—add subtle wear, bumps, or terrain‑like details instantly.

    Non‑destructive: Preview live, apply when ready, and iterate endlessly.


Dynamic Voxel Remeshing

    Quickly transform messy sculpts or boolean chaos into, volume‑preserving topology!

    Resolution up to 2048 — ideal for retopology on the fly.

    This retopology is voxel based. Recommended to be used on simple meshes to avoid artifacts.

    Note that higher resolution meshes take much longer to polish.



⚙️ Technical Notes:

    Performance: Powered by CPU‑optimized BMesh operations (Blender Python's native limitation). Blender Python natively does support GPU acceleration. This leads to much slower performance compared to claypolish tool in zbrush. Performance scales based on the CPU capabilities and poly count.
    Iterations: Iteration slider will multiply the operation time. 

    High polygon meshes: Polish becomes significantly slower on high polygons.

    Remeshing: Remeshing implemented is a simple voxel remeshing, to prioritize performance. However the resolution mapping is based on surface area. Which means the density output of the mesh will be similar to zbrush's Dynamesh.

    Requirements: Blender 4.3+. No external dependencies—install and sculpt



💡 Thank you for considering!


I crafted this tool during my own shift from ZBrush to Blender, filling the void with algorithms that mimic ClayPolish's magic but leverage BMesh for speed and safety

Its not ClayPolish, but its close!

I am dedicated to providing updates and improvements to the best of my ability! 

Updates will be released as needed to improve stability and usability.

Feel free to to get in touch in case of any feedback, bugs or suggestions!

Buying this add on also contributes to the Blender Development Fund! 



🔑 License

Released under GPL v3




## 🔗 Buy My Blender Add-on

- 🛒 [Available on Gumroad](https://gumroad.com/yourstore)
- 🧪 [Also on Superhive](https://blendermarket.com/yourproduct)




🎨 Sculpt smart.  Polish with a click!  
