---
title: Instalar o Azure PowerShell no Windows com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: c03c6ee3782b68de8a237b3c215405ff6513dbca
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523221"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Instalar o Azure PowerShell no Windows com o PowerShellGet

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Esse artigo explica as etapas para instalar os módulos do Azure PowerShell para o PowerShell 5.x do Windows usando o PowerShellGet. O PowerShellGet e o gerenciamento de módulos são os modos preferidos de instalação do Azure PowerShell, mas se você quiser instalar com o Web Platform Installer ou o pacote do MSI, consulte [Outros métodos de instalação](other-install.md).

Não há suporte para o modelo de implantação clássico do Azure desta versão do Azure PowerShell. Para obter suporte com as implantações clássicas, siga as instruções em [Instalar o módulo de Gerenciamento de Serviços do Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).

> [!IMPORTANT]
> Não há suporte para o módulo do AzureRM para macOS ou Linux. Para usar os cmdlets do Azure PowerShell nessas plataformas, [Instalar o módulo Az](/powershell/azure/install-az-ps).

## <a name="requirements"></a>Requisitos

Para instalar o Azure PowerShell, você precisa do PowerShellGet versão 1.1.2.0 ou superior. Para verificar se ele está disponível em seu sistema, execute o comando a seguir:

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -AllVersions | Select-Object -Property Name,Version,Path
```

Você deverá ver algo semelhante à seguinte saída:

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Se for necessário atualizar sua instalação do PowerShellGet, execute este comando:

```powershell-interactive
Install-Module PowerShellGet -Force
```

Se você não tiver o PowerShellGet instalado, siga as instruções referentes ao seu sistema na tabela abaixo.

|Cenário|Instalar instruções|
|---|---|
|Windows 10<br/>Windows Server 2016|Compilado no Windows Management Framework (WMF) 5.0 incluído no SO|
|Fazer upgrade para o PowerShell 5| <ol><li>[Instalar a versão mais recente do WMF](https://www.microsoft.com/download/details.aspx?id=54616)</li><li>Execute o comando a seguir:<br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> Usar o PowerShellGet requer uma Política de Execução que permite executar scripts. Para obter mais informações sobre a Política de Execução do PowerShell, consulte [Sobre as Políticas de Execução](/powershell/module/microsoft.powershell.core/about/about_execution_policies).
>
> [!IMPORTANT]
> O módulo descrito neste documento, AzureRM, usa o .NET Framework. Isso o torna incompatível com o PowerShell 6.0, que usa o .NET Core. Se você estiver usando o PowerShell 6.0, siga as [instruções de instalação para o macOS e o Linux](/powershell/azure/install-az-ps).

## <a name="install-the-azure-powershell-module"></a>Instalar módulo do Azure PowerShell

Você precisa de privilégios elevados para instalar os módulos da Galeria do PowerShell. Para instalar o Azure PowerShell, execute o comando a seguir em uma sessão elevada:

```powershell-interactive
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

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar. A importação automática do módulo `AzureRM` requer a configuração de um perfil do PowerShell. Saiba mais sobre isso em [Sobre Perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).
Para aprender a manter sua entrada no Azure entre as sessões, consulte [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Atualizar o módulo do Azure PowerShell

Você pode atualizar sua instalação do Azure PowerShell executando [Update-Module](/powershell/module/powershellget/update-module). Esse comando __não__ desinstala as versões anteriores.

```powershell-interactive
Update-Module -Name AzureRM
```

Se quiser remover as versões mais antigas do Azure PowerShell do sistema, consulte [Desinstalar o módulo do Azure PowerShell](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Usar várias versões do Azure PowerShell

É possível instalar diversas versões do Azure PowerShell. Talvez seja necessário mais de uma versão se você trabalhar com recursos locais do Azure Stack, executar uma versão anterior do Windows que não permite a atualização para o PowerShell 5.0 ou usar o modelo de implantação clássico do Azure. Para instalar uma versão mais antiga, forneça o argumento `-RequiredVersion` na instalação.

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

Ao carregar o módulo do Azure PowerShell, a versão mais recente é carregada por padrão. Para carregar uma versão diferente, forneça o argumento `-RequiredVersion`.

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a>Fornecer comentários

Se você encontrar um bug ao usar o Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).
Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).

## <a name="next-steps"></a>Próximas etapas

Para começar a usar o Azure PowerShell, consulte [Introdução ao Azure PowerShell](get-started-azureps.md) para saber mais sobre o módulo e seus recursos.
