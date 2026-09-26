# Image-to-3D Research

## 1. Problem Definition

**Goal:** Convert a single 2D image of an object into a 3D representation.

**Input:**
A single RGB image, preferably containing one clear object.

**Output:**
A 3D representation such as a Mesh, Point Cloud, or 3D Gaussian representation.

---

## 2. 3D Representations

### Point Cloud

A set of 3D points, where each point has coordinates `(x, y, z)`.

**Pros:** Simple and useful for representing 3D shape.
**Cons:** Does not explicitly represent surfaces.

### Mesh

A 3D surface consisting of:

* Vertices → points
* Edges → connections
* Faces → surfaces

**Pros:** Suitable for visualization and representing complete 3D surfaces.

### Voxel

A 3D grid made of small volumetric cells, similar to pixels but in 3D.

### 3D Gaussian

A representation based on 3D Gaussian primitives that can represent position, scale, color, and opacity.

---

## 3. Dataset Requirements

For our experiment, a useful dataset should ideally contain:

* 2D images of objects
* Corresponding 3D ground-truth models
* Single-object images
* Suitable image quality
* Compatible 3D formats

### Candidate Datasets

**ShapeNet:**
A large 3D object dataset containing categorized 3D models.

**Objaverse:**
A large and diverse collection of 3D objects from multiple sources.

The final dataset will be selected after identifying the Image-to-3D models we will use.

---

## 4. Evaluation Metrics

### Chamfer Distance (CD)

Measures the distance between the predicted and ground-truth 3D point sets.

**Lower = Better**

### F-score

Measures how well the predicted points match the ground-truth points using a distance threshold.

**Higher = Better**

### IoU

Measures the overlap between the predicted and ground-truth 3D volumes.

**Higher = Better**

---

## 5. Expected Experiment

```text
2D Image
   ↓
Image-to-3D Model
   ↓
Generated 3D
   ↓
Compare with Ground Truth
   ↓
CD / F-score / IoU
```

The exact experiment will depend on the models selected by the other team member.

---

## 6. Models

To be added after researching suitable Image-to-3D models.

| Model   | Input | Output | Representation | Pretrained |
| ------- | ----- | ------ | -------------- | ---------- |
| Model 1 | TBD   | TBD    | TBD            | TBD        |
| Model 2 | TBD   | TBD    | TBD            | TBD        |

---

## 7. Next Steps

1. Identify suitable Image-to-3D models.
2. Check their input/output requirements.
3. Select a compatible dataset.
4. Prepare preprocessing.
5. Run a small experiment.
6. Evaluate the generated 3D using suitable metrics.
7. Compare the tested approaches.
