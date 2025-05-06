# BackupManager (Backup Manager)

The BackupManager add-on provides functionality for creating and restoring backups of configuration files and certain directories.  
A key feature of this add-on is the ability to quickly create a backup of all directories and configuration files directly into the default folder.  
The manager also offers selective backup creation and selective restoration from backup files.

### Backup and restore options:

The following directories and configuration files can be backed up or restored:

* **SpeechDicts** directory  
* **Profiles** directory  
* **Scratchpad** directory  
* **RHVoice-config** directory  
* **ProfileTriggers** configuration file  
* **Gestures** configuration file  
* **NVDA** configuration file  

### Keyboard Shortcuts:

* **NVDA+Shift+B** тАУ Quick backup creation  
* **NVDA+Windows+B** тАУ Open the restore panel in the manager  
* **NVDA+Control+Shift+B** тАУ Open the backup creation panel in the manager  
* **NVDA+Alt+B** тАУ Open the backups folder  

All keyboard shortcuts can be modified in the Input Gestures dialog under the **"Backup Manager"** category.

The manager window can also be launched via the NVDA menu: **Tools тЖТ Backup Manager**.

### Manager Description:

The main dialog contains two panels:

* **Create**  
* **Restore**  

These panels can also be opened using their respective keyboard shortcuts.

#### Creating Backups

When the manager window opens, focus lands on the **"Create"** panel by default.  
This panel can also be accessed via its keyboard shortcut or through the **Tools** submenu.

Here, you can manually create backups by selecting the desired directories and files using checkboxes.  
Upon launch, the manager detects available directories and configuration files. If any are missing or empty, they will be disabled in the list.

After selecting the items to back up, click **"Start Creation"**.  
A file explorer window will open, prompting you to name the backup file and choose a save location.  
By default, the **"Backups"** folder in NVDA's user directory is suggested.  
Click **"Save"**, and a confirmation dialog will appear, indicating success or failure.  
Clicking **OK** returns you to the main manager window.  
You can close the manager by clicking **"Close"** or pressing the **Escape** key.

#### Restoring Backups

When the manager opens, focus is initially on the **"Create"** panel. Press the **Down Arrow** to navigate to the **"Restore"** panel.  
This panel can also be opened via its keyboard shortcut.

Here, click **"Start Restoration"**.  
A file explorer window will open, allowing you to select the backup file.  
By default, the **"Backups"** folder in NVDA's user directory is suggested.  
After selecting the file, click **"Open"**.  

**Note:**  
- You can press **Enter** on the selected backup file.  
- You can also paste a backup file path (copied to the clipboard earlier) into the filename field and click **"Open"**.  

If the backup file passes integrity checks, a list of restorable items will appear.  
Only items found in the backup will be available for selection.  
After marking the desired items, click **"Restore"**.  
A confirmation dialog will appear, and NVDA will restart to apply the restored configurations.  

#### Quick Backup Creation

This feature has no dedicated panel or settings.  
Pressing the **"Quick Backup"** shortcut (NVDA+Shift+B) creates a backup of all detected items in the default folder.  
After a few seconds, you will hear:  

> Quick backup successfully created: nvda_backup_2025-05-01_12-00-32.nvda-backup  

Backup filenames include the current date and time.

#### Opening the Backups Folder

The default folder is **"Backups"** in NVDA's user directory.  
Press the **"Open Backups Folder"** shortcut (NVDA+Alt+B) to open it.  

**Note:**  
Currently, the default folder location cannot be changed.

### Acknowledgments

Special thanks to the talented developer **H├йctor J. Ben├нtez Corredera**.  
This add-on is based on the backup functionality from **[AddonPackager](https://github.com/hxebolax/Add-on-packer)**.  

Unfortunately, the original developer discontinued support for this multifunctional add-on on **March 8, 2023** (version 1.5).  
I once requested additional backup-related features, but they were never implemented.  
Another programmer later took over, translating the code from Spanish to English and renaming the add-on, but no new functionality was added.  
Rather than contacting the new maintainer, I decided to implement the features myself, extracting the backup functionality into this standalone add-on.  
The Spanish **AddonPackager** code was translated to English and adapted for this purpose.  

### Changelog

#### 2025.04.30  
Initial release.  
