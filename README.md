# ENCoDE_tutorial
A tutorial for use on ENCoDE, a skin tone and pulse oximetry dataset, can be found here: https://colab.research.google.com/drive/1YqEfUMU366IfpC1eaTnmMres45wd8O52?usp=sharing

# Data Access
Data can be accessed through PhysioNet.org. Under the name: "ENCoDE, mEasuring skiN Color to correct pulse Oximetry DisparitiEs: skin tone and clinical data from a prospective trial on acute care patients". 

# Data Exploration
We have created a [Docker image](https://github.com/aiwonglab/ENCoDE_tutorial/pkgs/container/ares-encode) that contains characteristics and quality metrics for the ENCoDE dataset that can be visualized using the [ARES web application](https://github.com/OHDSI/Ares).
In order to run this image as a container on your local machine, you will need to:
  1. If you don't have it already, [install Docker](https://docs.docker.com/engine/install/)
  2. Execute the following command in your terminal to pull and launch the image:
     - `docker run --rm -p 7070:80 -d --name ares ghcr.io/aiwonglab/ares-encode:latest` (you may need to add `sudo` at the start of the command depending on your configuration)
  3. Open a new tab in your web browser and navigate to `localhost:7070` (or potentially, `127.0.0.1:7070`, or `0.0.0.0:7070` depending on your OS) to access the web application and start exploring
  4. When finished, run the following command to stop and remove the container:
     - `docker stop ares`
     
As we make updates to the dataset, we will plan to build their metadata into new versions of this same image; ARES allows you to explore and compare different data releases with regard to their quality and characteristics.
