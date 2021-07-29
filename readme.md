## Python Automation Test


### 1) The Script

We need to generated some documents, but this should be done automatically.
The files that need to be filled is the ```template.docx``` file. All information needed to generate this documents are in ```config.yaml```.

You should create a Python Script that looks for the information inside ```config.yaml``` file and generate a document based on ```template.docx```.
The script should be parametrized, so we will be able to change the output directory and the configuration file. The script must be called as described bellow.

```bash
$> python main.py -c [CONFIG-FILE] -o [OUTPUT-DIR]
```
or
```bash
$> python main.py --config [CONFIG-FILE] --output [OUTPUT-DIR]
```

The output must be a folder with N documents filled with the information within ```config.yaml```. The output file name must be  **[BAND_NAME]**.docx.

### 2) The Job

The automation must be triggerd by a jenkins job and the documents generated must be stored in job's artifact section. 
Our jenkins server does not contain ```pip``` or other libraries used in your automation, so the script must be in a Docker Image!


### Summary
  * A scipt that reads a yaml file and fill a document based in a template with the information.
  * A Docker Image containing the script and libraries used (so we don't have to worry about setting up an environment to run the automation).
  * A Jenkins Job that will run the container, execute the script and store the artifacts. 
