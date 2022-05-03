<h1>Azure Sentinel Lab - Log Failed RDP Attacks</h1>



<h2>Descrição</h2>
<b>O Script feito em Powershell nesse repositório é responsável por analisar as informações do Windows Event relacionadas a ataques RDP Brute Force (Remote Desktop Protocol). Quando atuando em conjunto com uma API de geolocalização aberta e com o Azure Sentinel configurado e conectado a uma máquina virtual atuando como honey pot, é capaz de mostrar as informações geográficas dos ataques e sua posição no mapa mundi do Azure Sentinel.
</b>

<br />
<br />
<h3>Principais pontos do projeto:</h3>
<br />

- Desenvolvimento de script PowerShell personalizado para extrair metadados do Windows Event Viewer e fazer o encaminhamento à API open source para tratar os
dados e mostrar geolocalização dos eventos.<br /><br />
- Configuração do Log Analytics Workspace no Azure para inserir logs personalizados contendo informações geográficas (Latitude, Longitude, Estado e País).<br /><br />
- Configuração de campos personalizados no Log Analytics Workspace do Azure para mapeamento de dados geográficos no Azure Sentinel.<br /><br />
- Configuração do Azure Sentinel (Cloud SIEM) workbook para exibir ataques globais (RDP brute force) em um mapa de acordo com a localização e magnitude dos
ataques.<br /><br />
- Criação e configuração de máquinas virtuais no Azure
<br />
<br />


<p align="center">
<img src="https://i.imgur.com/3d3CEwZ.png" height="85%" width="85%" alt="RDP event fail logs to iP Geographic information"/>
</p>
<br />
<p align="center">
<img src="https://i.imgur.com/lzuZc1b.png" height="85%" width="85%" alt="RDP event fail logs to iP Geographic information"/>
</p>
<br />
<p align="center">
<img src="https://i.imgur.com/s2iIBGv.png" height="85%" width="85%" alt="RDP event fail logs to iP Geographic information"/>
</p>
<br />
<h2>Linguagens</h2>

- <b>PowerShell:</b> Extração dos logs de Logon do Windows Event Viewer

<h2>Utilidades</h2>

- <b>ipgeolocation.io:</b> Retorna informações geográficas de um determinado IP

<h2>Ataques vindo da Russia sendo registrados em log com informações geográficas</h2>

<p align="center">
<img src="https://i.imgur.com/7gutzhV.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<h2>Mapa Mundi mostrando últimos ataques RDP registrados ao redor do mundo com informações geográficas.</h2>

<p align="center">
<img src="https://i.imgur.com/fWoHC9w.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
