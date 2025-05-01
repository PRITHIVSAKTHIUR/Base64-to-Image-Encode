# Base64 to Image Converter

This project provides a simple web interface built with Gradio to convert Base64 encoded strings into viewable images. It uses Python with the Pillow library for image processing.

**GitHub Repository:** [https://github.com/PRITHIVSAKTHIUR/Base64-to-Image-Encode](https://github.com/PRITHIVSAKTHIUR/Base64-to-Image-Encode)

## Overview

The application takes a Base64 string as input (either raw or with a data URI scheme like `data:image/png;base64,...`) and decodes it to display the corresponding image directly in the web interface.

## Features

* **Simple Web UI:** Easy-to-use interface powered by Gradio.
* **Data URI Support:** Automatically removes the `data:image/...;base64,` header if present.
* **Error Handling:** Provides feedback if the Base64 string is invalid or if the data cannot be converted to an image.
* **Image Conversion:** Ensures the final displayed image is in RGB format using Pillow.
* **Example Inputs:** Includes clickable examples directly in the UI for easy testing.

## Requirements

* Python 3.x
* Gradio
* Pillow (PIL fork)

## Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/PRITHIVSAKTHIUR/Base64-to-Image-Encode.git](https://github.com/PRITHIVSAKTHIUR/Base64-to-Image-Encode.git)
    cd Base64-to-Image-Encode
    ```

2.  **Install the required libraries:**
    ```bash
    pip install gradio Pillow
    ```
    *(Note: The `base64` and `io` modules are part of the Python standard library and don't require separate installation.)*

## Usage

1.  **Run the Python script:**
    *(Assuming you saved the provided code as `app.py` or similar)*
    ```bash
    python app.py
    ```

2.  **Access the Interface:**
    The script will start a local web server and print a URL (usually `http://127.0.0.1:7860` or similar). Open this URL in your web browser.

3.  **Convert Base64:**
    * Paste your Base64 encoded string into the input text box.
    * Alternatively, click one of the provided examples below the input box.
    * Click the "Submit" button.
    * The decoded image will appear in the output area. If there's an error, an error message will be displayed instead.

## Code Structure

* `base64_to_image(b64_string: str)`: The core function that handles the Base64 decoding and image conversion. It performs error checking for URI format, decoding, and image opening.
* `gr.Interface(...)`: Sets up the Gradio web interface, linking the `base64_to_image` function to the text input and image output components.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please feel free to open an issue or submit a pull request.
