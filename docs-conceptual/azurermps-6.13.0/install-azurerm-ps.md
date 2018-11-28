---
title: Instalar o Azure PowerShell no Windows com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 0830f3e00f85d3b69eff9a999bdb6c3e952cf360
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259359"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Instalar o Azure PowerShell no Windows com o PowerShellGet

Este artigo explica as etapas para instalar os módulos do Azure PowerShell em um ambiente Windows usando o PowerShellGet. O PowerShellGet e o gerenciamento de módulos são os modos preferidos de instalação do Azure PowerShell, mas se você quiser instalar com o Web Platform Installer ou o pacote do MSI, consulte [Outros métodos de instalação](other-install.md).

Para obter instruções de instalação do Azure PowerShell em outras plataformas, consulte [Instalar e configurar o Azure PowerShell no macOS e no Linux](install-azurermps-maclinux.md).

Não há suporte para o modelo de implantação clássico do Azure desta versão do Azure PowerShell. Para obter suporte com as implantações clássicas, siga as instruções em [Instalar o módulo de Gerenciamento de Serviços do Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).

[!INCLUDE[az-replacing-azurerm](../includes/az-replacing-azurerm.md)]

## <a name="requirements"></a>Requisitos

Começando com o Azure PowerShell versão 6.0, o Azure PowerShell requer o PowerShell versão 5.0. Para verificar a versão do PowerShell em execução no computador, execute o seguinte comando:

```powershell-interactive
$PSVersionTable.PSVersion
```

Se você tiver uma versão desatualizada, consulte [Atualizar o Windows PowerShell existente](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

> [!IMPORTANT]
> O módulo descrito neste documento, AzureRM, usa o .NET Framework. Isso o torna incompatível com o PowerShell 6.0, que usa o .NET Core. Se você estiver usando o PowerShell 6.0, siga as [instruções de instalação para o macOS e o Linux](install-azurermps-maclinux.md).

## <a name="install-the-azure-powershell-module"></a>Instalar módulo do Azure PowerShell

Você precisa de privilégios elevados para instalar os módulos da Galeria do PowerShell. Para instalar o Azure PowerShell, execute o comando a seguir em uma sessão elevada:

```powershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> Caso sua versão seja mais antiga que a 2.8.5.201 do NuGet, será necessário baixar e instalar a versão mais recente do NuGet.

Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet. Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Responda `Yes` ou `Yes to All` para continuar a instalação.

O módulo `AzureRM` é um módulo de rollup para os cmdlets do Azure PowerShell. A instalação dele baixa todos os módulos disponíveis do Azure Resource Manager e possibilita usar seus cmdlets.

## <a name="sign-in"></a>Entrar

Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> Se você desabilitou o carregamento automático do módulo, precisará importar manualmente o módulo com `Import-Module AzureRM`. Por causa da maneira como o módulo está estruturado, isso pode levar alguns segundos.


Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar. Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Atualizar o módulo do Azure PowerShell

Você pode atualizar sua instalação do Azure PowerShell executando [Update-Module](/powershell/module/powershellget/update-module). Esse comando __não__ desinstala as versões anteriores.

```powershell-interactive
Update-Module -Name AzureRM
```

Se quiser remover as versões mais antigas do Azure PowerShell do sistema, consulte [Desinstalar o módulo do Azure PowerShell](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Usar várias versões do Azure PowerShell

É possível instalar mais de uma versão do Azure PowerShell. Para verificar se você tem diversas versões do Azure PowerShell instaladas, use o seguinte comando:

```powershell-interactive
Get-Module -Name AzureRM -List | select Name,Version
```

Para remover uma versão do Azure PowerShell, confira [Desinstalar módulo do Azure PowerShell](uninstall-azurerm-ps.md).

Talvez seja necessário mais de uma versão se você trabalhar com recursos locais do Azure Stack, executar uma versão anterior do Windows ou usar o modelo de implantação clássico do Azure. Para instalar uma versão mais antiga, forneça o argumento `-RequiredVersion` na instalação.

```powershell-interactive
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

Ao carregar o módulo do Azure PowerShell, a versão mais recente é carregada por padrão. Para carregar uma versão diferente, forneça o argumento `-RequiredVersion`.

```powershell-interactive
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a>Fornecer comentários

Se você encontrar um bug ao usar o Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).
Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).

## <a name="next-steps"></a>Próximas etapas

Para começar a usar o Azure PowerShell, consulte [Introdução ao Azure PowerShell](get-started-azureps.md) para saber mais sobre o módulo e seus recursos.