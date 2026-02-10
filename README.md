# Computer Vision Course - Insper

**Undergraduate Computer Vision Course**  
**Duration:** 14 weeks  
**Format:** ~30 min lecture + 1.5 hours hands-on lab per week  
**Prerequisites:** Python programming, Linear Algebra  

## Course Overview

This course provides a comprehensive introduction to computer vision, covering both classical computer vision techniques and modern deep learning approaches. Students will learn fundamental concepts of image processing, feature detection, and neural networks, culminating in a final project that demonstrates their mastery of computer vision techniques.

## Reference Materials

- **Primary Textbook:** Gonzalez & Woods - Digital Image Processing
- **Secondary Reference:** [MIT Vision Textbook](https://visionbook.mit.edu)
- **Framework:** PyTorch (for deep learning components)

## Course Structure

The course is divided into three main segments:

1. **Weeks 1-4:** Foundations (Image basics, color, neural networks)
2. **Weeks 5-9:** Classical Computer Vision (Filtering, features, transformations)
3. **Weeks 10-14:** Deep Learning + Final Project

### Weekly Schedule

| Week | Topic | Lecture | Lab | Project |
|------|-------|---------|-----|---------|
| 1 | Introduction to Computer Vision | What is vision? Applications, image representation | Python/NumPy refresher, image I/O | - |
| 2 | Neural Networks Basics | Perceptrons, backpropagation, basic architectures | Implement simple NN in PyTorch | - |
| 3 | Color Perception and Models | Human vision, RGB, HSV, color spaces | Color space transformations, histogram analysis | - |
| 4 | Brightness and Contrast | Intensity transformations, histogram equalization | Image enhancement techniques | - |
| 5 | Advanced Neural Networks | CNNs, activation functions, optimization | Build and train a CNN in PyTorch | **Project proposal due** |
| 6 | Image Smoothing and Filtering | Gaussian blur, median filter, convolution | Implement custom filters, noise reduction | Work on project |
| 7 | Discrete Derivatives | Sobel, Prewitt, gradient computation | Edge detection implementation | - |
| 8 | Scale Space and Pyramids | Gaussian pyramids, scale-invariant features | Multi-scale processing | - |
| 9 | Corner Detection and Features | Harris, SIFT, feature descriptors | Keypoint detection and matching | **Midterm checkpoint** |
| 10 | Geometric Transformations | Homography, affine transforms, RANSAC | Image warping and stitching | Work on project |
| 11 | Deep Neural Networks | ResNet, batch norm, transfer learning | Fine-tune pretrained models | - |
| 12 | Advanced Topics | Non-linearity, modern architectures | Experiment with architectures | Work on project |
| 13 | Final Project Work | - | - | **Full project work** |
| 14 | Final Presentations | Student presentations | - | **Final delivery** |

## Learning Objectives

By the end of this course, students will be able to:

- Understand fundamental concepts of digital image representation and processing
- Implement classical computer vision algorithms (filters, edge detection, feature matching)
- Design and train neural networks for vision tasks using PyTorch
- Apply geometric transformations and camera models
- Develop a complete computer vision application from conception to deployment
- Critically analyze and compare different approaches to vision problems

## Assessment

- **Lab Assignments:** 25%
- **Final Project:** 75%

## Getting Started

### Environment Setup

1. **Install Python 3.8+**

2. **Create a virtual environment:**
```bash
python -m venv cv_env
source cv_env/bin/activate  # On Windows: cv_env\Scripts\activate
```

3. **Install required packages:**
```bash
pip install -r requirements.txt
```

### Required Packages

- PyTorch >= 2.0
- torchvision
- NumPy
- OpenCV (cv2)
- Matplotlib
- Pillow
- scikit-image
- Jupyter

### Prerequisites

This repository uses **Git LFS** (Large File Storage) for lecture PDFs, images, and videos.

**⚠️ You MUST install Git LFS before cloning, or files won't download correctly!**

### Step 1: Install Git LFS (One-Time Setup)

Choose your operating system:

<details>
<summary><b>macOS (with Homebrew)</b></summary>

```bash
brew install git-lfs
git lfs install
```
</details>

<details>
<summary><b>macOS (without Homebrew - Apple Silicon M1/M2/M3)</b></summary>

```bash
# Download and install
cd ~/Downloads
curl -L https://github.com/git-lfs/git-lfs/releases/download/v3.4.1/git-lfs-darwin-arm64-v3.4.1.tar.gz -o git-lfs.tar.gz
tar -xzf git-lfs.tar.gz
sudo cp git-lfs-3.4.1/git-lfs /usr/local/bin/
sudo chmod +x /usr/local/bin/git-lfs
rm -rf git-lfs-3.4.1 git-lfs.tar.gz

# Initialize
git lfs install
```
</details>

<details>
<summary><b>Windows</b></summary>

1. Download installer from: https://git-lfs.github.com/
2. Run the installer (it will add Git LFS to your Git installation)
3. Open Git Bash or Command Prompt and run:
```bash
git lfs install
```
</details>

<details>
<summary><b>Linux (Ubuntu/Debian)</b></summary>

```bash
sudo apt-get update
sudo apt-get install git-lfs
git lfs install
```
</details>

<details>
<summary><b>Linux (Fedora/RHEL)</b></summary>

```bash
sudo yum install git-lfs
git lfs install
```
</details>

### Step 2: Verify Installation

```bash
git lfs version
```

You should see something like: `git-lfs/3.4.1`

### Step 3: Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/computer-vision.git
cd computer-vision
```

**LFS files (PDFs, images, videos) will download automatically during clone!**

### Step 4: Install Python Dependencies

```bash
# Create virtual environment
python -m venv cv_env
source cv_env/bin/activate  # On Windows: cv_env\Scripts\activate

# Install packages
pip install -r requirements.txt
```

### Troubleshooting

<details>
<summary><b>Problem: Files show as "version https://git-lfs.github.com/spec/v1" instead of actual content</b></summary>

**Cause:** Git LFS wasn't installed before cloning

**Solution:**
```bash
# Install Git LFS (see Step 1 above)
git lfs install

# Pull the actual files
git lfs pull
```

All files should now download correctly!
</details>

<details>
<summary><b>Problem: "git-lfs: command not found"</b></summary>

**Cause:** Git LFS not in PATH

**Solution:**

macOS/Linux - Add to `~/.zshrc` or `~/.bash_profile`:
```bash
export PATH="/usr/local/bin:$PATH"
```

Then reload:
```bash
source ~/.zshrc  # or source ~/.bash_profile
```

Windows - Reinstall Git LFS and ensure "Add to PATH" is checked
</details>

<details>
<summary><b>Problem: Clone is very slow</b></summary>

**Cause:** Downloading large LFS files

**This is normal!** The repository includes:
- 12 lecture PDFs (~10MB)
- Lab images and videos
- Sample datasets

Be patient, it only happens once.
</details>

### What Gets Downloaded?

When you clone, Git LFS automatically downloads:
- ✅ Lecture slides (PDF format)
- ✅ Lab images and test data
- ✅ Video demonstrations
- ✅ Pre-trained model weights
- ✅ Sample datasets

Total size: ~50-100 MB (depending on materials)

### For Teaching Assistants

If you're setting up the repository for the first time:

```bash
# After cloning, verify all LFS files downloaded
git lfs ls-files

# Should show all PDFs, images, etc.
# If any are missing:
git lfs pull
```

## Course Policies

### Attendance
Regular attendance is expected. Labs are hands-on and build upon each other.

### Academic Integrity
All work must be your own. You may discuss concepts with classmates, but code and write-ups must be individual. For the final project, teams of 2-3 are allowed.

### Late Policy
- Labs: 10% deduction per day late (max 3 days)
- Project milestones: No late submissions accepted

## Office Hours

TBD - To be announced in first class

## Contact

For questions, please use the course discussion forum or email the instructor.

---

*Last updated: February 2026*
