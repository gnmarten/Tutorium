## Spacy under Windows  

The following will take up ca. 5 GB of harddrive space.  
  
Install [Anaconda](https://docs.anaconda.com/anaconda/install/windows/)  
(We DO "recommend adding Anaconda to the PATH environment variable", da es sich so einfacher bedienen lässt.)  

```
If missing, in Windows: edit “system variables” to add Anaconda to path  
"Edit the system environment variables" --> "Environment variables" --> "User variables for administrator" --> "Path" --> "Edit" --> "New" -->
```  
Add these as separate new lines  
```
C:\Users\**yourusername**\AppData\Local\Continuum\anaconda3\Scripts  
C:\Users\**yourusername**\AppData\Local\Continuum\anaconda3  
```
  
Open Anaconda Navigator with “elevated permissions” (as administrator)  
Create "new environment"/, give it a name without spaces and open “terminal” from there  
[Optional: remove any existing/old Spacy installlations =<2.0.16 with "pip uninstall spacy" or through Anaconda Navigator (by removing Numpy)]  
  
Install spacy through Navigator or manually:  
```conda install -c conda-forge spacy
python -m spacy info   
python -m spacy download en_core_web_sm  
python -m spacy download de_core_news_sm  
python -m spacy download en_core_web_md  
python -m spacy validate  
```
--> If the last step shows:  
"You may also want to overwrite the incompatible links using the `python -m spacy  
link` command with `--force`, or remove them from the data directory. Data path: ..."  
  
```python -m spacy link en_core_web_sm en  
python -m spacy link de_core_news_sm de
```
  
in Windows, you may have to create the directories "en" and "de" manually by adding a link to the physical location of the language models as "New: shortcut" in:   
```
C:\Users\**yourusername**\AppData\Local\Continuum\anaconda3\envs\python36\lib\site-packages\spacy\data 
```

Open the commandline via the Anaconda Navigator Interface as follows:  

Actually running Spacy in a Jupyter Notebook may require one to first install Jupyter via this command (if ipython and jupyter are not available for installation in Anaconda Navigator) --> replace myenv with the name of your environment.  
```
conda install -n myenv ipython jupyter
```

Some users may experience problems setting the Jupyter to their environment. In this case, the following might be necessary:  
```
conda install -c anaconda ipykernel
python -m ipykernel install --user --name=myenv  #replace myenv with the name of your environment.
```

Installation of the module "pip install wordfreq" requires C++ Build Tools to be installed by downloading [Visual Studio Tools for Windows](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=BuildTools&rel=16) and then selecting C++ tools in the menu to be installed. (This will take up an extra 5 Gb of harddrive space!) The system will install marisa-trie without moaning afterwards.  

Installation of German Bert is dependent on installation of Pytorch via Anaconda.  
```
python -m spacy download de_trf_bertbasecased_lg
```

## Other software


Es wäre von Vorteil, wenn man von zu Hause bereits die benötigten Software-Pakete herunterladen und installieren könnte:

 

0. UGent VPN

[https://helpdesk.ugent.be/vpn/](https://helpdesk.ugent.be/vpn/)

 

1. LanguageTool Free

[https://languagetoolplus.com/](https://languagetoolplus.com/)

LanguageTool Plugin for Chrome

[https://chrome.google.com/webstore/detail/grammar-and-spell-checker/oldceeleldhonbafppcapldpdifcinji](https://chrome.google.com/webstore/detail/grammar-and-spell-checker/oldceeleldhonbafppcapldpdifcinji)

LibreOffice

[https://nl.libreoffice.org/](https://nl.libreoffice.org/)

LanguageTool for LibreOffice

[https://extensions.libreoffice.org/extensions/languagetool/4.8](https://extensions.libreoffice.org/extensions/languagetool/4.8)

 

2. Zotero Standalone + Chrome Connector

[https://www.zotero.org/download/](https://www.zotero.org/download/)

 

 

3. R(evolutions) statistical software
RStudio Desktop Open Source

[https://rstudio.com/products/rstudio/#rstudio-desktop](https://rstudio.com/products/rstudio/#rstudio-desktop)

--> RStudio befindet sich auch online auf Athena

 

4. Github Desktop

[https://desktop.github.com/](https://desktop.github.com/) --> Passwort erstellen bei github.com!

 

Optional

5. VMware Workstation 15 Player (nicht für Mac)

[https://www.vmware.com/go/getplayer-win](https://www.vmware.com/go/getplayer-win)

 

Wer am eigenen Gerät (unter Windows) über mindestens 40 GB Freiraum verfügt, kann sich gerne auch eine virtuelle Maschine herunterladen, die diese Software-Pakete schon enthält: Wer mir eine Email schickt, bekommt den Link dazu.


<!-- Docs to Markdown version 1.0β18 -->
