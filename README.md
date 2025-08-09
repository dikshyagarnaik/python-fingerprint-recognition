# Python Fingerprint Recognition

Fingerprint recognition with SKimage and OpenCV

Requirements:
- NumPy
- SKimage
- OpenCV2


Works by extracting minutiae points using harris corner detection.

Uses SIFT (ORB) go get formal descriptors around the keypoints with brute-force hamming distance and then analyzes the returned matches using thresholds.

Usage:

1. Place 2 fingerprint images that you want to compare inside the database folder
2. Pass the names of the images as arguments in the console

## Dockerfile

If you don't want to install the libraries, or want a easier way to test the application you can follow the commands:

```shell
docker build -t <name_of_your_choice> .

docker run -it <name_of_your_choice> <fingerprint_1> <fingerprint_2>
```

If you don't have Docker Engine installed, you can get the instructions to install it here: [Install Docker](https://docs.docker.com/v17.09/engine/installation/)

NOTE: the fingerprints must be in the `/database` folder

## Credits

Special thanks to https://github.com/Utkarsh-Deshmukh/Fingerprint-Enhancement-Python for providing a library used to enhance the fingerprint picture.

## My Notes on Running This Project

I forked this repository to learn about fingerprint recognition with Python and OpenCV.

### Steps I Followed
1. Cloned the repo locally.
2. Created a Python virtual environment.
3. Installed dependencies with `pip install -r requirements.txt`.
4. Ran the program with sample fingerprint images from the `/database` folder.

Example command:
```bash
python src/fingerprint_recognition.py database/101__M_Left_index_finger.BMP database/102__M_Left_index_finger.BMP

