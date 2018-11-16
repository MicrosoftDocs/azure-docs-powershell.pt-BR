---
title: Outras maneiras de instalar o Azure PowerShell | Microsoft Docs
description: Como instalar o Azure PowerShell usando o pacote MSI ou o Web Platform Installer.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 5016c7e768aba94308d0e78785481fafbac36c74
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/15/2018
ms.locfileid: "51575375"
---
# <a name="other-installation-methods"></a>Outros métodos de instalação

O Azure PowerShell tem vários métodos de instalação. O uso do PowerShellGet com a Galeria do PowerShell é o método preferencial. O Azure PowerShell pode ser instalado no Windows usando o Web Platform Installer (WebPI) ou usando o MSI de arquivo disponível no GitHub.

## <a name="install-on-windows-using-the-web-platform-installer"></a>Instalar no Windows usando o Web Platform Installer

A instalação do Azure PowerShell mais recente do WebPI é feita da mesma maneira como era nas versões anteriores.
Baixe o [pacote WebPI do Azure PowerShell](http://aka.ms/webpi-azps) e inicie a instalação.

> [!NOTE]
> Se você já tiver instalado módulos do Azure da Galeria do PowerShell, o instalador os removerá automaticamente. Isso simplifica a seu ambiente, garantindo que apenas uma versão do Azure PowerShell está instalada. No entanto, há cenários em que será necessário ter diversas versões instaladas ao mesmo tempo.
>
> Os módulos da Galeria do PowerShell instalam módulos no `$env:ProgramFiles\WindowsPowerShell\Modules`. Por outro lado, o instalador do WebPI instalam os módulos do Azure no `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.
>
> Se ocorrer um erro durante a instalação, você poderá remover manualmente as pastas do Azure* de sua pasta `$env:ProgramFiles\WindowsPowerShell\Modules` e tentar instalar novamente.

Quando a instalação for concluída, a configuração do `$env:PSModulePath` deverá incluir os diretórios que contêm os cmdlets do Azure PowerShell. O comando a seguir pode ser usado para verificar se o Azure PowerShell foi instalado corretamente.

```powershell-interactive
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> Há um problema conhecido que pode ocorrer durante a instalação do WebPI. Se o computador precisar de uma reinicialização devido a atualizações do sistema ou outras instalações, isso poderá fazer com que as atualizações do `$env:PSModulePath` falhem ao incluir o caminho em que o Azure PowerShell está instalado.

Ao tentar carregar ou executar cmdlets após a instalação, você poderá receber a seguinte mensagem de erro:

```output
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

Esse erro pode ser corrigido ao reiniciar o computador ou importar o módulo usando o caminho totalmente qualificado. Por exemplo: 

```powershell-interactive
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a>Instalar no Windows usando o pacote MSI

O Azure PowerShell pode ser instalado usando o arquivo MSI disponível no [GitHub](https://github.com/Azure/azure-powershell/releases/latest). Se você tiver versões anteriores dos módulos do Azure instaladas, o instalador as removerá automaticamente. O pacote MSI instala módulos no `$env:ProgramFiles\WindowsPowerShell\Modules`, mas não cria pastas específicas de versão.

