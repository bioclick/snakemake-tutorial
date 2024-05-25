# What is Snakemake
Snakemake is a workflow management system used primarily in bioinformatics and data science for defining and executing complex data analysis workflows. It is designed to facilitate reproducibility, scalability, and flexibility in scientific workflows. Here is a detailed explanation of Snakemake, covering its key features, components, and usage alongside with sptep by step guide for its setup.

## Organization of files and folders
Using a specified folder structure helps to understand the project better. Therefore, it is recommended to follow some conventions in order to keep things nice and neat. First, let's create some files and directories to begin with:
Change directory to your snakemake project:
```bash
cd PATH/TO/YOUR/SNAKEMAKE-POJECT
```
Creating directories:
```bash
mkdir src out log sandbox
```
Creating files:
```bash
touch README.md Snakefile
```

Now, your project structure should look like this:
```bash
./
    |- src/
    |- out/
    |- log/
    |- sandbox/
    README.md
    Snakefile
```

- `Root (./):` This is the main folder of the project. Everything that is used or produced for the project should be located in a this folder.

- `src:` This is the ‘source’ folder. It contains all of your code files you develop during your analysis and the original datasets you begin your analysis with.

- `out:` This is the output directory. We will put anything that we create by running a Python script.

- `log:` When we run a python script, it produces output and messages, typically printing them to the screen. If we want to save those messages to a file, so we can refer to them in the future, we will save them here.

- `sandbox:` As we work through our project, we will want to explore new ideas and test out how to code them. While we play with these bits and pieces of code, we save them in the sandbox. Separating them from src means we know that scripts in here are ‘under development’. When they are finalized, we can move them into src.

- `README.md:` A README is a file that introduces and explains the project. We should write information that explains what the project is about and how someone can run the scripts developed for the project in this file. We also recommend providing installation instructions to clarify exactly what needs to be installed to run the project.

- `Snakefile:` We will use the Snakefile to write the steps needed that run all the scripts in the project. 

You can check your project's contents by using `ls` command:
```bash
ls
```