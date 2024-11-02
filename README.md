# instructlab-knowledge-docs

```
mkdir ~/idemo
cd ~/idemo
python3.11 -m venv venv

# Add environment variables to the environment that instructlab does NOT use the XDG directory scheme
# Otherwise it will put the files (config, taxonomy, etc) in ~/.local/share, ~/.config and ~/.cache directories
# This is very odd to edit and was not the case before instructLab version 0.19
 
echo "export XDG_DATA_HOME=~/idemo" >> ./venv/bin/activate
echo "export XDG_CONFIG_HOME=~/idemo" >> ./venv/bin/activate
echo "export XDG_CACHE_HOME=~/idemo" >> ./venv/bin/activate

# Activate the virtual environment
source ./venv/bin/activate

# Download and install InstructLab
pip3 install instructlab

# Check if it is running
ilab --version

# Initialize Instruct Lab
ilab config init

# Download model
ilab model download

# Serve the model
ilab serve

# in another terminal (don't forget to source ./venv/bin/activate !!) open a chat to the model
ilab chat
```

