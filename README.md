# README

## Project: 3D Cube Rendering (with Camera Rotation)

### Overview

This project renders images of a 3D cube from different angles by rotating the camera around it. The rendered images are saved in a directory and zipped for easy download and sharing.

### Dependencies

- Python 3.x
- Numpy
- Pillow (PIL)

### Files

- `render_cube.py`: The main script for rendering the 3D cube images.

### Installation

1. Ensure you have Python 3 installed.
2. Install the required libraries:
    ```bash
    pip install numpy pillow
    ```

### Usage

1. **Run the script**:
    ```bash
    python render_cube.py
    ```
    This script will create a directory named `renders_pillow` where the images of the cube from different angles will be saved.

2. **Script Functionality**:
    - Defines the vertices and edges of a cube.
    - Normalizes vectors and calculates cross products for vector math.
    - Sets up the camera and projection matrices.
    - Iterates through a range of radii and steps to create a rotating camera effect.
    - Projects the vertices of the cube onto a 2D plane and draws the edges.
    - Saves each rendered frame as an image in the `renders_pillow` directory.

3. **Output**:
    - The rendered images are saved in the `renders_pillow` directory.
    - The images are copied to the `/cube_images_fixed` directory.
    - A zip archive of the images is created at `/cube_images_fixed.zip`.

### Directory Structure

- `renders_pillow`: Directory where the rendered images are saved.
- `/cube_images_fixed`: Directory where images are copied for zipping.
- `/cube_images_fixed.zip`: Zip archive containing the rendered images.

### Example Output

The script will render images of a cube as seen from different angles by moving the camera in a circular path around the cube. Each image represents a different view angle of the stationary cube.

### Customization

- **Field of View (FOV)**: Adjust the `fov` variable to change the field of view of the camera.
- **Aspect Ratio**: Change the `aspect_ratio` variable to adjust the aspect ratio of the projection.
- **Radius Range**: Modify the `radius_range` variable to change the range of radii for the camera's circular path.
- **Number of Steps**: Change the `num_steps` variable to alter the number of steps (frames) in one complete rotation.

### Notes

- Ensure the output directories exist before running the script.
- The script will automatically create the directories if they do not exist.
