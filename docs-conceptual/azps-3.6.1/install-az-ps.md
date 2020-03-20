---
title: Instalar o Azure PowerShell com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/26/2020
ms.openlocfilehash: 7a25270566f5e856ee44c4c191a47a3e7334508b
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/11/2020
ms.locfileid: "79110986"
---
# <a name="install-azure-powershell"></a>Instalar o Azure PowerShell

Este artigo explica como instalar os módulos do Azure PowerShell usando o PowerShellGet. Essas instruções funcionam nas plataformas Windows, macOS e Linux.

O Azure PowerShell também está disponível no Azure [Cloud Shell](/azure/cloud-shell/overview) e agora é pré-instalado em [imagens do Docker](azureps-in-docker.md).

## <a name="requirements"></a>Requisitos

O Azure PowerShell funciona com o PowerShell 5.1 ou superior no Windows ou com o PowerShell Core 6.x e posterior em todas as plataformas. Você deve instalar a [versão mais recente do PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core) disponível para seu sistema operacional. O Azure PowerShell não tem requisitos adicionais quando executado no PowerShell Core.

Para verificar sua versão do PowerShell, execute o comando:

```powershell-interactive
$PSVersionTable.PSVersion
```

Para usar o Azure PowerShell no PowerShell 5.1 no Windows:

1. Atualize para o [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) se necessário. Se você estiver usando o Windows 10, você já tem o PowerShell 5.1 instalado.
2. Instale o [.NET Framework 4.7.2 ou posterior](/dotnet/framework/install).
3. Verifique se tem a versão mais recente do PowerShellGet. Execute `Update-Module PowerShellGet -Force`.

## <a name="install-the-azure-powershell-module"></a>Instalar módulo do Azure PowerShell

O uso dos cmdlets do PowerShellGet é o método de instalação preferencial. Esse método funciona da mesma forma nas plataformas Windows, macOS e Linux. Execute o seguinte comando em uma sessão do PowerShell:

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet. Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Responda `Yes` ou `Yes to All` para continuar a instalação.

O módulo Az é um módulo de rollup para os cmdlets do Azure PowerShell. A instalação dele baixa todos os módulos disponíveis do Azure Resource Manager e possibilita usar seus cmdlets.

> [!WARNING]
> Não há compatibilidade na instalação dos módulos AzureRM e Az no PowerShell 5.1 para Windows ao mesmo tempo. Caso você precise manter o AzureRM disponível no sistema, instale o módulo Az para o PowerShell Core 6.x ou posterior.

Primeiro, [instale o PowerShell Core 6.x ou posterior](/powershell/scripting/install/installing-powershell-core-on-windows)

Em seguida, em uma sessão do PowerShell Core, instale o módulo Az somente para o usuário atual. Este é o escopo de instalação recomendado.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

A instalação do módulo para todos os usuários de um sistema requer privilégios elevados. Inicie a sessão do PowerShell usando **Executar como administrador** no Windows ou use o comando `sudo` no macOS ou Linux:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

## <a name="install-offline"></a>Instalar offline

Em alguns ambientes, não é possível se conectar à Galeria do PowerShell. Nessas situações, você ainda pode instalar offline usando um destes métodos:

* Baixe os módulos em outro local da sua rede e use-os como uma origem de instalação.
  Isso permite que você armazene módulos do PowerShell em cache em um único servidor ou compartilhamento de arquivo para serem implantados com o PowerShellGet em sistemas desconectados. Saiba como configurar um repositório local e instalar em sistemas desconectados com [Trabalhar com repositórios PowerShellGet locais](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).
* [Baixe o MSI (Microsoft Windows Installer) do Azure PowerShell](install-az-ps-msi.md) em um computador conectado à rede e, em seguida, copie o instalador para sistemas sem acesso à Galeria do PowerShell. Tenha em mente que o instalador do MSI só funciona para PowerShell 5.1 no Windows.
* Salve o módulo com [Save-Module](/powershell/module/PowershellGet/Save-Module) em um compartilhamento de arquivo ou salve-o em outra fonte e copie-o manualmente para outros computadores:

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>Solução de problemas

Estes são alguns problemas comuns observados durante a instalação do módulo do Azure PowerShell. Caso você tenha um problema que não foi listado aqui, [registre um problema no GitHub](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Conexão de blocos de proxy

Se você obtiver erros de `Install-Module` que indicam que a Galeria do PowerShell está inacessível, talvez você esteja protegido por um proxy. Sistemas operacionais e ambientes de rede diferentes têm requisitos diferentes para configurar um proxy para todo o sistema. Entre em contato com o administrador do sistema para obter as configurações de proxy e saber como defini-las para seu ambiente.

O PowerShell em si pode não ser configurado para usar esse proxy automaticamente. Com o PowerShell 5.1 e posterior, configure a sessão do PowerShell para usar um proxy por meio dos seguintes comandos:

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

Caso suas credenciais do sistema operacional estejam configuradas corretamente, essa configuração roteará as solicitações do PowerShell por meio do proxy. Para manter essa configuração entre as sessões, adicione os comandos ao seu [perfil do PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).

Para instalar o pacote, o proxy precisa permitir conexões HTTPS com o seguinte endereço:

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>Entrar

Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> Se você desabilitou o carregamento automático do módulo, importe manualmente o módulo com `Import-Module Az`. Por causa da maneira como o módulo está estruturado, isso pode levar alguns segundos.

Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar. Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Atualizar o módulo do Azure PowerShell

Para atualizar qualquer módulo do PowerShell, você deve usar o mesmo método usado para instalar o módulo. Por exemplo, caso tenha usado `Install-Module` originalmente, você deverá usar [Update-Module](/powershell/module/powershellget/update-module) para obter a versão mais recente. Caso tenha usado originalmente o pacote MSI, você deverá baixar e instalar o novo pacote MSI.

Os cmdlets do PowerShellGet não podem atualizar os módulos que foram instalados por meio de um pacote MSI. Os pacotes MSI não atualizam módulos que foram instalados usando o PowerShellGet. Se você tiver problemas ao atualizar usando o PowershellGet, deverá **reinstalar**, em vez de **atualizar**. A reinstalação é feita da mesma forma que a instalação, mas você precisa adicionar o parâmetro `-Force`:

```powershell
Install-Module -Name Az -AllowClobber -Force
```

Diferentemente das instalações baseadas em MSI, instalar ou atualizar usando o PowerShellGet não remove as versões mais antigas que possam existir em seu sistema. Para remover as versões antigas do Azure PowerShell do sistema, confira [Desinstalar o módulo do Azure PowerShell](uninstall-az-ps.md). Para obter mais informações sobre instalações baseadas em MSI, consulte [Instalar o Azure PowerShell com um MSI](install-az-ps-msi.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Usar várias versões do Azure PowerShell

É possível instalar mais de uma versão do Azure PowerShell. Para verificar se você tem diversas versões do Azure PowerShell instaladas, use o seguinte comando:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

Para remover uma versão do Azure PowerShell, confira [Desinstalar módulo do Azure PowerShell](uninstall-az-ps.md).

Se você tiver mais de uma versão do módulo instalada, o carregamento automático do módulo e o `Import-Module` carregarão a versão mais recente por padrão.

Você pode instalar ou carregar uma versão específica do módulo `Az` usando o parâmetro `-RequiredVersion`:

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="provide-feedback"></a>Fornecer comentários

Se você encontrar um bug no Azure PowerShell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues). Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Próximas etapas

Para saber mais sobre os módulos do Azure PowerShell e seus recursos, confira [Introdução ao Azure PowerShell](get-started-azureps.md). Se você estiver familiarizado com o Azure PowerShell e precisar migrar do AzureRM, confira [Migrar do AzureRM para Az](migrate-from-azurerm-to-az.md).
