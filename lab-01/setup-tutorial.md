There are many ways to set up a Python development environment, but one of the most popular combinations is using Miniconda as a package manager and PyCharm as an Integrated Development Environment (IDE).

This tutorial will guide you through the process of installing Miniconda, setting up PyCharm, and configuring them to work together.

## Table of Contents
- [Step 1: Install Miniconda](#step-1-install-miniconda)
  - [1.1 Download Miniconda](#11-download-miniconda)
  - [1.2 Install Miniconda](#12-install-miniconda)
    - [On Windows](#on-windows)
    - [On macOS/Linux](#on-macoslinux)
  - [1.3 Verify Installation](#13-verify-installation)
  - [1.4 Update Conda](#14-update-conda)
- [Step 2: Install PyCharm IDE](#step-2-install-pycharm-ide)
    - [2.1 Download PyCharm](#21-download-pycharm)
    - [2.2 Install PyCharm](#22-install-pycharm)
        - [On Windows](#on-windows-1)
        - [On macOS](#on-macos)
        - [On Linux](#on-linux)
    - [2.3 Initial Setup](#23-initial-setup)
- [Step 3: Setting Up PyCharm with Miniconda](#step-3-setting-up-pycharm-with-miniconda)
    - [3.1 Create a Python Project in PyCharm](#31-create-a-python-project-in-pycharm)
    - [3.2 Verify the Setup](#32-verify-the-setup)
- [Step 4: Conda Environment Setup (Optional but Recommended)](#step-4-conda-environment-setup-optional-but-recommended)
    - [4.1 Create a New Conda Environment](#41-create-a-new-conda-environment)
    - [4.2 Install Packages](#42-install-packages)


---

## Step 1: Install Miniconda

Miniconda is a lightweight distribution of Python that includes the conda package manager, which makes it easy to manage Python packages and environments.

### 1.1 Download Miniconda

- Go to the official [Miniconda download page](https://docs.conda.io/en/latest/miniconda.html).
- Choose the installer based on your operating system:
  - **Windows**: Download the `.exe` file for 64-bit or 32-bit Windows.
  - **macOS**: Download the `.pkg` file for macOS.
  - **Linux**: Download the `.sh` file for Linux (usually 64-bit).

### 1.2 Install Miniconda

#### On Windows:
1. Double-click the downloaded `.exe` file to launch the installer.
2. Follow the prompts in the installation wizard:
   - **Installation Type**: Choose "Just Me" unless you need it for all users.
   - **Destination Folder**: Choose the default path or specify your own.
   - **Add Miniconda to PATH**: It’s recommended to check the option "Add Miniconda to my PATH environment variable" for easier command-line usage.
   - **Register Miniconda as the default Python**: Select this option if you want Miniconda to be your primary Python version.

#### On macOS/Linux:
1. Open a terminal.
2. Navigate to the directory where the Miniconda `.sh` file is saved (e.g., `Downloads`):
   ```bash
   cd ~/Downloads
   ```
3. Run the installer script:
   ```bash
   bash Miniconda3-latest-Linux-x86_64.sh  # For Linux
   bash Miniconda3-latest-MacOSX-x86_64.sh  # For macOS
   ```
4. Follow the on-screen instructions, and ensure you allow the script to initialize Miniconda in your shell.

### 1.3 Verify Installation

After installation, open a terminal or Command Prompt and run:
```bash
conda --version
```
You should see the version number of conda, confirming the successful installation.

### 1.4 Update Conda

To ensure you have the latest version of conda, run:
```bash
conda update conda
```

---

## Step 2: Install PyCharm IDE

PyCharm is an Integrated Development Environment (IDE) developed by JetBrains that is great for Python development.

### 2.1 Download PyCharm

- Visit the official [PyCharm download page](https://www.jetbrains.com/pycharm/download/).
- Choose the appropriate version based on your operating system:
  - **Windows/macOS/Linux**.
- Select the **Community** edition (free) unless you need features from the Professional edition.

### 2.2 Install PyCharm

#### On Windows:
1. Run the `.exe` installer you downloaded.
2. Follow the setup instructions:
   - **Install for**: Choose either "All Users" or "Just Me".
   - **Destination Folder**: You can keep the default folder.
   - **Options**: It’s recommended to check:
     - “Create Desktop Shortcut” for easier access.
     - “Add ‘Open Folder as Project’” if you want to open directories with PyCharm from the context menu.
3. Click “Install” and complete the setup.

#### On macOS:
1. Open the downloaded `.dmg` file.
2. Drag and drop PyCharm into the **Applications** folder.
3. Launch PyCharm from the Applications folder.

#### On Linux:
1. Extract the downloaded `.tar.gz` file in the terminal:
   ```bash
   tar -xzf pycharm-community-*.tar.gz
   ```
2. Navigate to the extracted folder and run:
   ```bash
   cd pycharm-community-*/bin
   ./pycharm.sh
   ```

### 2.3 Initial Setup

1. When you first launch PyCharm, you’ll be prompted with some setup options:
   - Choose whether to send anonymous statistics to JetBrains (optional).
   - Select a UI theme: Light/Dark based on your preference.
2. You’ll be taken to the **Welcome Screen** where you can create new projects or open existing ones.

---

## Step 3: Setting Up PyCharm with Miniconda

### 3.1 Create a Python Project in PyCharm

1. Open PyCharm, click **New Project**.
2. In the **New Project** window:
   - Set the project location.
   - Choose **Conda** as the environment.
   - If PyCharm doesn’t detect Miniconda, click on the gear icon next to the **Base Interpreter** field and navigate to where Miniconda was installed (e.g., `~/miniconda3/bin/python`).
   - Click **Create**.

### 3.2 Verify the Setup

1. Inside your new project, create a new Python file by right-clicking on the project folder, selecting **New**, and then **Python File**.
2. Write a simple Python script, such as:
   ```python
   print("Hello, world!")
   ```
3. Run the script by right-clicking on the file and selecting **Run**.

---

## Step 4: Conda Environment Setup (Optional but Recommended)

### 4.1 Create a New Conda Environment

1. Open a terminal or Command Prompt.
2. Create a new environment by running:
   ```bash
   conda create --name myenv python=3.9
   ```
   Replace `myenv` with the name of your environment. For example, you can name it `comp1010`.

3. Activate your environment:
   ```bash
   conda activate myenv
   ```

4. To use this environment in PyCharm, go to **File** > **Settings** (or **Preferences** on macOS) > **Project** > **Python Interpreter**, click the gear icon, and choose **Add**. Then select **Conda Environment** and choose the environment you just created.

### 4.2 Install Packages

To install packages (e.g., NumPy), run:
```bash
conda install numpy
```
Or in PyCharm, go to the **Python Packages** tool window, search for the package, and click **Install**.

This will happen during the later stages of the course related to machine learning topics.

---