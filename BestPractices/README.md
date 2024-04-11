Abra o Tabular Editor.
Conecte em algum modelo.
Rode o código abaixo na janela de Script Avançado.
```c#
System.Net.WebClient w = new System.Net.WebClient(); 

string path = System.Environment.GetFolderPath(System.Environment.SpecialFolder.LocalApplicationData);
string url = "https://raw.githubusercontent.com/cabelo-moreno/TabularEditor/main/BestPractices/Portuguese/BPARules.json";
string version = System.Windows.Forms.Application.ProductVersion.Substring(0,1);
string downloadLoc = path+@"\TabularEditor\BPARules.json";

if (version == "3")
{
    downloadLoc = path+@"\TabularEditor3\BPARules.json";
}

w.DownloadFile(url, downloadLoc);
```


Alternativa 2:
Na barra de Pesquisa do Windows, digite %LocalAppData%
Abra essa pasta, depois localize a pasta do Tabular Editor e dentro dela salve o arquivo BPARules.Json

![image](https://github.com/cabelo-moreno/TabularEditor/assets/77420876/0ba3d9f3-ab69-4fd3-8536-986cbc65d64e)
