---
title: Outras maneiras de instalar o Azure PowerShell
description: Como instalar o Azure PowerShell usando o pacote MSI ou o Web Platform Installer.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323315"
---
# <a name="other-installation-methods"></a>Outros métodos de instalação

Este artigo explica como instalar o Azure PowerShell usando uma MSI ou o Web Platform Installer (WebPI). Você também pode executar o Azure PowerShell de dentro de um contêiner do Docker. Use esses métodos de instalação somente se eles forem necessários para o seu sistema. A maneira canônica para instalar o Azure PowerShell é através do PowerShellGet. Para obter instruções sobre como usar o PowerShellGet para instalar o Azure PowerShell, confira [Instalar o Azure PowerShell com o PowerShellGet](install-azurerm-ps.md).

Para instalar em ambientes Linux ou macOS, confira [Instalar o Azure PowerShell no macOS ou Linux](install-azurermps-maclinux.md).

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>Instalar ou atualizar no Windows usando o Web Platform Installer

A instalação do Azure PowerShell mais recente do WebPI é feita da mesma maneira como era nas versões anteriores.
Baixe o [pacote WebPI do Azure PowerShell](http://aka.ms/webpi-azps) e inicie a instalação.

> [!NOTE]
> Se você já tiver instalado módulos do Azure da Galeria do PowerShell, o instalador os removerá automaticamente. Isso simplifica a seu ambiente, garantindo que apenas uma versão do Azure PowerShell está instalada. No entanto, há cenários em que será necessário ter diversas versões instaladas ao mesmo tempo.
>
> Os módulos da Galeria do PowerShell instalam módulos no `$env:ProgramFiles\WindowsPowerShell\Modules`. Por outro lado, o instalador do WebPI instalam os módulos do Azure no `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.
>
> Se ocorrer um erro durante a instalação, você poderá remover manualmente as pastas do `Azure*` de sua pasta `$env:ProgramFiles\WindowsPowerShell\Modules` e tentar instalar novamente.

Quando a instalação for concluída, a configuração do `$env:PSModulePath` deverá incluir os diretórios que contêm os cmdlets do Azure PowerShell. O comando a seguir pode ser usado para verificar se o Azure PowerShell foi instalado corretamente:

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> Há um problema conhecido que pode ocorrer durante a instalação do WebPI. Se o computador precisar de uma reinicialização devido a atualizações do sistema ou outras instalações, isso poderá fazer com que as atualizações do `$env:PSModulePath` falhem ao incluir o caminho em que o Azure PowerShell está instalado.

Ao tentar carregar ou executar cmdlets após a instalação, você poderá receber a seguinte mensagem de erro:

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

Esse erro pode ser corrigido ao reiniciar o computador ou importar o módulo usando o caminho totalmente qualificado.

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Instalar ou atualizar no Windows usando o pacote MSI

O Azure PowerShell pode ser instalado usando o arquivo MSI disponível no [GitHub](https://aka.ms/azps-release). Se você tiver versões anteriores dos módulos do Azure instaladas, o instalador as removerá automaticamente. O pacote MSI instala módulos no `$env:ProgramFiles\WindowsPowerShell\Modules`, mas não cria pastas específicas de versão.

## <a name="run-in-a-docker-container"></a>Executar em um contêiner do Docker

Vamos manter um conjunto de imagens do Docker pré-configuradas no Azure PowerShell. Há dois tipos de contêineres disponíveis: os que estão executando o PowerShell tradicional no Windows, e um contêiner executando o PowerShell Core no Windows ou no Linux.

| Ambiente | Imagem do Docker |
|-------------|--------------|
| PowerShell no Windows | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| PowerShell Core no Windows | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| PowerShell Core no Linux | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Para executar qualquer um desses contêineres, você deve usar `docker run -it $ImageName` para obter um terminal interativo. Por exemplo, para executar o PowerShell Core no contêiner do Linux, use:

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> Para executar um contêiner do Windows no Docker, o sistema operacional do host deve ser Windows e o Docker deve ser definido para executar contêineres do Windows. Para obter informações sobre como alternar entre ambientes Windows e Linux no Docker, confira a documentação do Docker [Alternar entre contêineres do Windows e do Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).