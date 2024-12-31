# ML-PyTorch_fast.ai devcontainer

This devcontainer
- Begins with Microsoft's Miniconda (Python 3) devcontainer image
- Adds Jupyter notebook support
- Updates conda, installs and configures the libmamba solver, installs PyTorch, and installs fast.ai--with Nvidia GPU support

Before using VSCode to develop remotely in a container, please install these VSCode extensions locally:
  - **Remote Development** extension, by Microsoft
  - **Dev Containers** extension, by Microsoft

## To develop in this devcontainer: ##
### Option A-Cloning from GitHub: ###
1. If you haven't yet configured Arthur to connect to GitHub via SSH, please follow these instructions first: https://github.com/jimgta/ninja/blob/main/README.md#one-time-setup-to-connect-to-github-with-ssh
2. In VS Code, connect to Arthur and then click the **Clone Repository** button in the Explorer tab.
3. Paste the SSH address for this repo `git@github.com:jimgta/ML-PyTorch_fast.ai.git` into the top textbox and press **Enter**.
4. Select or type the location of a remote directory to use for the repo clone: for example /home/[username]/projects/
5. After the cloned files download and appear in the Explorer view, click **Reopen in Container** in the dialog box that appears in the lower-right corner.

### Option B-Copying from Arthur's /home/gta directory: ###
> [!NOTE]
> If you use this option, your copied files will *not* remain synced with the GTA repo.
1. In VS Code, connect to Arthur and click **Open Folder** to open a remote directory for development (e.g., /home/[username]/projects/projectA).
2. Open a terminal and make sure you are currently in your chosen development directory.
3. Copy files from /home/gta/devcontainers/ML-PyTorch_fast.ai to your current directory using the following command:
    ```
    rsync -r --exclude .git /home/gta/devcontainers/ML-PyTorch_fast.ai/ .
    ```
4. Type `Ctrl+Shift^P` to open the Command Palette.
5. Type and select **Dev Containers: Reopen in Container...**

### Then: ###
1. Your new container should start running after a minute or two.  If you want, click **Starting Dev Container (show log)** in the dialog box that appears to see the progress. After the new container loads, you can being coding.
    - If you followed Option A above, after the new container loads, click the small source control button called **main** in the bottom status bar (next to the colored Dev Container label). Then click **Create new branch** in the top textbox that appears to         create a new branch and begin coding.
2. To begin coding next time, you can 1) connect to Arthur, 2) click **Open Folder** to open your remote directory for develpment (e.g., /home/[username]/projects/projectA), and 3) click **Reopen in Container** in the dialog box that appears in the lower-right corner.

## To develop in a vanilla Miniconda (Python 3) devcontainer *without* the above additions/updates: ##
1. In VS Code, connect to Arthur and then click **Open Folder** to choose a local directory for development.
2. After the folder opens, type `Ctrl+Shift^P` to open the Command Palette.
3. Type and select **Dev Containers: Reopen in Container...**
4. Type and select **Miniconda (Python 3)** as the starting point for your container.
5. Then select **Create Dev Container**.
6. After the new container loads, you can being coding.
- Reference: https://code.visualstudio.com/docs/devcontainers/containers#_quick-start-open-an-existing-folder-in-a-container
