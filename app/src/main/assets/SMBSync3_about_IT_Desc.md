## Funzione  
SMBSync3 è uno strumento per sincronizzare i file tra la memoria interna del dispositivo Android, MicroSD, USB Flash e PC/NAS tramite LAN wireless utilizzando il protocollo SMB1, SMB2 o SMB3. <span style="color: red;"><u>La sincronizzazione è unidirezionale</u></span> dalla cartella di origine a quella di destinazione e può essere riflessa, spostata, copiata o archiviata.  
La sincronizzazione periodica può essere avviata dalla funzione di programmazione di SMBSync3 o da applicazioni esterne (Tasker, AutoMagic, ecc.).  
- Specchio  
Le répertoire et les fichiers sources sont copiés de manière différentielle (<u>***1**</u>) vers la destination, et une fois la copie terminée, les fichiers et répertoires qui n'existent pas du côté source sont supprimés.  
- Spostare  
La directory di origine e i file vengono copiati in modo differenziale(<u>*****1**</u>) sul lato di destinazione, e i file sul lato di origine vengono cancellati quando la copia è completata. (Tuttavia, il file con lo stesso nome, la dimensione del file e la data modificata sono gli stessi nel lato di origine e di destinazione, e il file non viene copiato, e la directory di origine e il file vengono cancellati dopo che la copia è terminata. lato del file).  
- Copia  
Delta-copia(<u>***1**</u>) i file contenuti nella directory di origine verso la destinazione.  
- Archivio  
Foto e video contenuti nella directory dei sorgenti con data e ora di 7 giorni dalla data di esecuzione dell'archivio Vai a destinazione prima o prima di 30 giorni, ecc. (Ma non è possibile utilizzare lo ZIP per la destinazione).  

<u>***1**</u> Il file di differenza è una delle tre condizioni seguenti.  

1. Il file non esiste  
2. Diverse dimensioni dei file  
3. Diverso rispetto all'ultimo aggiornamento di 3 secondi  

### Manuali  
[FAQs](https://sentaroh.github.io/Documents/SMBSync3/SMBSync3_FAQ_EN.htm)  
[Description](https://sentaroh.github.io/Documents/SMBSync3/SMBSync3_Desc_EN.htm)  
