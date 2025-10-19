# Ai- un chat-bot per il nostro liceo

Questo è un progetto scolastico, che sarà presentato al JRC di Ispra.

Il progetto è volto alla realizzazione di un chat bot che possa fungere da "assistente digitale" della scuola,
può fornire varie informazioni sulla scuola che possono essere utili agli utenti del nostro liceo.

## LLama - un passo fondamentale

abbiamo utilizzato llama per scaricare una versione base di gemma 3.1, lo abbiamo poi "personalizzato" secondo le nostre esigenze

### COME INSTALLARE LLAMA IN LOCALE:

1. andare sul sito "https://www.llama.com/llama-downloads/"
2. seguire tutti i passaggi sul sito
3. quando vi dirà "In your preferred environment run the command below": dovete copiare e incollare quei comandi nel "prompt dei comandi" sul vostro pc
   (per trovarlo schiacciate il tasto windows e digitate "prompt dei comandi)
4. continuate a seguire i passaggi sul sito e come versione da scaricare scegliete "Llama3.3-70B-Instruct
5. dopodichè vi dirà di inserire il link che riceverete via mail dopo aver inserito la vostra mail sul sito che vi ho scritto all'inizio
6. copiate e incollate il link ricevuto via mail sul prompt dei comandi e partirà il download

### La "personalizzazione":

per "personalizzare" il nostro chat bot abbiamo utilizzato un metodo non legato al machine learning poichè sarebbe stato troppo complicato, e noi studenti non avevamo le competenze per farlo. Quindi per fare ciò, abbiamo fatto in modo che (tramite uno script python) che prima di rispondere ad ogni domanda, il chat bot leggesse un file .txt che gli davamo "in pasto" per fargli avere le informazioni del nostro liceo.
