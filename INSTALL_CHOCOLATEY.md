# Instalação do Chocolatey

Para instalar o chocolatey no seu sistema, abra uma janela do _PowerShell_ com permições de administrador e execute esse comando:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

Se nem um erro for exibido, o chocolatey já está dispível no seu sistema.

Feche a janela do terminal, e execute, em uma nova janela, o seguinte comando para testar:

```powershell
choco -?
```

Um manual completo de como usar o Chocolatey pode ser encontrado [aqui](https://chocolatey.org/docs/getting-started).

<br/>
<br/>

[⬅️ Voltar a instalação do git](./INSTALL_GIT.md).
