# Image to Sketch

This project (titled **Image to Sketch**) implements an assignment from the LGM Data Science Virtual Internship featured on the Startascratch website. The full Python code is provided in this repository for reference, modification, and reuse.

---

## Project Origin

- **Source:** LGM Data Science Virtual Internship on Startascratch (https://platform.stratascratch.com/data-projects/image-pencil-sketch)
- **Goal:** Transform any RGB image into a pencil-sketch-style rendering using OpenCV’s image-processing functions.

---

## Assignment Details

1. **Grayscale Conversion**: Turn the RGB input into a classic black-and-white photo.  
2. **Inversion**: Create a negative of the grayscale image to emphasize highlights.  
3. **Blurring**: Apply Gaussian blur to the inverted image, simulating pencil diffusion.  
4. **Color-Dodge Blend**: Divide the grayscale image by the blurred inversion to generate the pencil-stroke effect.  
5. **Experimentation**: Optionally add or swap filters (e.g. bilateral filter, adaptive thresholding) for custom artistic styles.

---

## Data Description

- **Sample Image:** `dog.jpg` (included).  
- **Alternate Inputs:** Any valid RGB image may be used—just update the filename in `sketch.py` or pass it as a parameter.

---

## Repository Contents

```
├── datasets/
│   └── dog.jpg                      # Sample image
├── image_to_pencil_sketch.ipynb     # Notebook with annotated code walkthrough
├── image_to_pencil_sketch.py        # Main script implementing the pipeline
├── requirements.txt                 # List of Python dependencies
├── README.md                        # This documentation
└── .gitignore                       # Git ignore rules
```

---


## Requirements

All required packages are listed in `requirements.txt`. To install them in one step:

```bash
pip install -r requirements.txt
```

Here’s what you’ll find in `requirements.txt`:
```text
numpy>=1.19.0
opencv-python>=4.5.0      # or opencv-python-headless for non-GUI environments
matplotlib>=3.3.0
```

---

## Running the Code

1. **Clone** or **download** this repository.  
2. **Install dependencies** via the requirements file:  
   ```bash
   pip install -r requirements.txt
   ```
3. **Place** your chosen image in the datasets folder (default: `dog.jpg`).  
4. **Run** the sketch pipeline:  
   ```bash
   python image_to_pencil_sketch.py
   ```
5. **View** the output: a Matplotlib window will display the original and sketched images side by side.

---

## Achievements & Highlights

- **Modular Pipeline:** Each image-processing step lives in its own function for readability and easy extension.  
- **Single-call API:** `pencil_sketch(path, blur_kernel)` ties everything together with minimal boilerplate.  
- **Customizable:** Adjust the blur kernel or insert new filters to experiment with different sketch styles.  
- **Extensible:** Clear separation of concerns makes it trivial to add enhancements (e.g., edge overlay, thresholding).

---

Each function is documented to show the purpose of that transformation. For full code, see `sketch.py`.

---

Feel free to raise issues, suggest enhancements, or contribute new filters! Happy sketching!