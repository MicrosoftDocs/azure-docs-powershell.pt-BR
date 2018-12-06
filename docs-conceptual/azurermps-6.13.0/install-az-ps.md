---
title: Instalar “Az” do Azure PowerShell com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet no Windows, macOS e Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/26/2018
ms.openlocfilehash: 3d52b18750341f220dc8e10d6bf89796457c5a10
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52826775"
---
# <a name="install-the-azure-powershell-az-module"></a>Instalar módulo “Az” do Azure PowerShell

Este artigo informa como instalar os módulos do Azure PowerShell usando o PowerShellGet. Essas instruções funcionam nas plataformas Windows, macOS e Linux. A versão de visualização do Az, não há suporte para nenhum outro método de instalação. 

## <a name="requirements"></a>Requisitos

O Azure PowerShell funciona com o PowerShell 5.x no Windows ou o PowerShell 6.x em qualquer plataforma. Para verificar a versão do PowerShell em execução no computador, execute o seguinte comando:

```powershell-interactive
$PSVersionTable.PSVersion
```

Se você tiver uma versão desatualizada ou precisar instalar o PowerShell, confira [Instalando várias versões do PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6). As informações de instalação para sua plataforma estão vinculadas a partir dessa página.

## <a name="install-the-azure-powershell-module"></a>Instalar módulo do Azure PowerShell

> [!IMPORTANT]
>
> É possível ter ambos os módulos `AzureRM` e `Az` instalados ao mesmo tempo. Caso tenha ambos os módulos instalados, __não habilite aliases__.
> Habilitar aliases causa conflitos entre os cmdlets `AzureRM` e os aliases de comando `Az`, podendo levar a comportamentos inesperados.
> Antes de instalar o módulo `Az`, recomenda-se desinstalar o `AzureRM`. É possível desinstalar o `AzureRM` ou habilitar aliases a qualquer momento. Para obter instruções de desinstalação, consulte [Desinstalar o módulo do Azure PowerShell (AzureRM)](uninstall-azurerm-ps.md). 

Para instalar os módulos em um escopo global, você precisa de privilégios elevados para instalar os módulos da Galeria do PowerShell. Para instalar o Azure PowerShell, execute o seguinte comando em uma sessão elevada ("Executar como Administrador" no Windows ou com privilégios de superusuário no macOS ou no Linux):

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

Se você não tiver acesso aos privilégios de administrador, você pode instalar para o usuário atual adicionando o argumento `-Scope`.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet. Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Responda `Yes` ou `Yes to All` para continuar a instalação.

O módulo `Az` é um módulo de rollup para os cmdlets do Azure PowerShell. A instalação dele baixa todos os módulos disponíveis do Azure Resource Manager e possibilita usar seus cmdlets.

## <a name="sign-in"></a>Entrar

Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Se você desabilitou o carregamento automático do módulo, precisará importar manualmente o módulo com `Import-Module Az`. Por causa da maneira como o módulo está estruturado, isso pode levar alguns segundos.

Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar. Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Atualizar o módulo do Azure PowerShell

Você pode atualizar sua instalação do Azure PowerShell executando [Update-Module](/powershell/module/powershellget/update-module). Esse comando __não__ desinstala as versões anteriores.

```powershell-interactive
Update-Module -Name Az
```

Se quiser remover as versões mais antigas do Azure PowerShell do sistema, consulte [Desinstalar o módulo do Azure PowerShell](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Usar várias versões do Azure PowerShell

É possível instalar mais de uma versão do Azure PowerShell. Para verificar se você tem diversas versões do Azure PowerShell instaladas, use o seguinte comando:

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

Para remover uma versão do Azure PowerShell, confira [Desinstalar módulo do Azure PowerShell](uninstall-azurerm-ps.md).

Você pode carregar uma versão específica do módulo `Az` usando o argumento `-RequiredVersion` com `Install-Module` e `Import-Module`:

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

Se tiver mais de uma versão do módulo instalada, a versão mais recente será carregada por padrão.

## <a name="provide-feedback"></a>Fornecer comentários

Se você encontrar um bug ao usar o Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).
Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.profile/send-feedback).

## <a name="next-steps"></a>Próximas etapas

Para começar a usar o Azure PowerShell, consulte [Introdução ao Azure PowerShell](get-started-azureps.md) para saber mais sobre o módulo e seus recursos.
