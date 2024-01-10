
## How to run Jupyter Notebook in .venv

To ensure that Jupyter Notebook uses the Python interpreter from your virtual environment (`.venv`), you need to create a kernel associated with that environment. Here's how you can do it:

1. **Activate Your Virtual Environment**: First, make sure your virtual environment is activated. In your terminal, navigate to your project directory and then activate the virtual environment. For a `.venv` folder, the command is usually:
   
   ```bash
   source .venv/bin/activate  # On Linux/macOS
   .venv\Scripts\activate     # On Windows
   ```

2. **Install Jupyter in the Virtual Environment**: If you haven't installed Jupyter Notebook within your virtual environment, install it now:

   ```bash
   pip install notebook
   ```

3. **Install `ipykernel`**: This package is necessary to create a new kernel for Jupyter. Install it using pip:

   ```bash
   pip install ipykernel
   ```

4. **Create a New Kernel**: Now, create a new kernel for Jupyter Notebook that uses the Python interpreter from your virtual environment. You can name this kernel to easily identify it later. For example:

   ```bash
   python -m ipykernel install --user --name=myenvkernel
   ```

   Replace `myenvkernel` with a name you prefer.

5. **Start Jupyter Notebook**: Run Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

6. **Select Your Kernel**: In Jupyter Notebook, open a notebook or create a new one. Then, change the kernel to the one you just created. You can do this by clicking on `Kernel` -> `Change kernel` -> `myenvkernel` (or the name you chose).

This process creates a kernel that is specific to your virtual environment, and whenever you select this kernel in Jupyter Notebook, it will use the Python interpreter and packages from your virtual environment.
