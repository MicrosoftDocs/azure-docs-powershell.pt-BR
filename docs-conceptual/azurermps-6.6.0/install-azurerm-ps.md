---
title: Instalar o Azure PowerShell no Windows com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: 50b05e5f25b6e3e1c815f6b26f1b53b84cd0b7da
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/02/2018
ms.locfileid: "39368068"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Instalar o Azure PowerShell no Windows com o PowerShellGet

Este artigo explica as etapas para instalar os módulos do Azure PowerShell em um ambiente Windows usando o PowerShellGet. O PowerShellGet e o gerenciamento de módulos são os modos preferidos de instalação do Azure PowerShell, mas se você quiser instalar com o Web Platform Installer ou o pacote do MSI, consulte [Outros métodos de instalação](other-install.md).

Para obter instruções de instalação do Azure PowerShell em outras plataformas, consulte [Instalar e configurar o Azure PowerShell no macOS e no Linux](install-azurermps-maclinux.md).

Não há suporte para o modelo de implantação clássico do Azure desta versão do Azure PowerShell. Para obter suporte com as implantações clássicas, siga as instruções em [Instalar o módulo de Gerenciamento de Serviços do Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).

## <a name="requirements"></a>Requisitos

Começando com o Azure PowerShell versão 6.0, o Azure PowerShell requer o PowerShell versão 5.0. Para verificar a versão do PowerShell em execução no computador, execute o seguinte comando:

```powershell
$PSVersionTable.PSVersion
```

Se você tiver uma versão desatualizada, consulte [Atualizar o Windows PowerShell existente](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

> [!IMPORTANT]
> O módulo descrito neste documento, AzureRM, usa o .NET Framework. Isso o torna incompatível com o PowerShell 6.0, que usa o .NET Core. Se você estiver usando o PowerShell 6.0, siga as [instruções de instalação para o macOS e o Linux](install-azurermps-maclinux.md).

## <a name="install-the-azure-powershell-module"></a>Instalar módulo do Azure PowerShell

Você precisa de privilégios elevados para instalar os módulos da Galeria do PowerShell. Para instalar o Azure PowerShell, execute o comando a seguir em uma sessão elevada:

```powershell
Install-Module -Name AzureRM
```

> [!NOTE]
> Caso sua versão seja mais antiga que a 2.8.5.201 do NuGet, será necessário baixar e instalar a versão mais recente do NuGet.

Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet. Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Responda `Yes` ou `Yes to All` para continuar a instalação.

O módulo `AzureRM` é um módulo de rollup para os cmdlets do Azure PowerShell. A instalação dele baixa todos os módulos disponíveis do Azure Resource Manager e possibilita usar seus cmdlets.

## <a name="sign-in"></a>Entrar

Para começar a trabalhar com o Azure PowerShell, você precisa carregar `AzureRM` em sua sessão atual do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure.

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar. A importação automática do módulo `AzureRM` requer a configuração de um perfil do PowerShell. Saiba mais sobre isso em [Sobre Perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).
Para aprender a manter sua entrada no Azure entre as sessões, consulte [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Atualizar o módulo do Azure PowerShell

Você pode atualizar sua instalação do Azure PowerShell executando [Update-Module](/powershell/module/powershellget/update-module). Esse comando __não__ desinstala as versões anteriores.

```powershell
Update-Module -Name AzureRM
```

Se quiser remover as versões mais antigas do Azure PowerShell do sistema, consulte [Desinstalar o módulo do Azure PowerShell](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Usar várias versões do Azure PowerShell

É possível instalar diversas versões do Azure PowerShell. Talvez seja necessário mais de uma versão se você trabalhar com recursos locais do Azure Stack, executar uma versão anterior do Windows que não permite a atualização para o PowerShell 5.0 ou usar o modelo de implantação clássico do Azure. Para instalar uma versão mais antiga, forneça o argumento `-RequiredVersion` na instalação.

```powershell
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

Ao carregar o módulo do Azure PowerShell, a versão mais recente é carregada por padrão. Para carregar uma versão diferente, forneça o argumento `-RequiredVersion`.

```powershell
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a>Fornecer comentários

Se você encontrar um bug ao usar o Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).
Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).

## <a name="next-steps"></a>Próximas etapas

Para começar a usar o Azure PowerShell, consulte [Introdução ao Azure PowerShell](get-started-azureps.md) para saber mais sobre o módulo e seus recursos.