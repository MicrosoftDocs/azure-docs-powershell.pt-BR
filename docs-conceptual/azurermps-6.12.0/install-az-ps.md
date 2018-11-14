---
title: Instalar o Azure PowerShell com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: c4af07816aaa6713d67e3349a45880f8cc22c80a
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/08/2018
ms.locfileid: "51276023"
---
# <a name="install-azure-powershell-with-powershellget"></a>Instalar o Azure PowerShell com o PowerShellGet

Este artigo informa como instalar os módulos do Azure PowerShell usando o PowerShellGet. A versão de visualização do Az, não há suporte para nenhum outro método de instalação. 

## <a name="requirements"></a>Requisitos

O Azure PowerShell funciona com o PowerShell 5.x no Windows ou o PowerShell 6.x em qualquer plataforma. Para verificar a versão do PowerShell em execução no computador, execute o seguinte comando:

```powershell-interactive
$PSVersionTable.PSVersion
```

Se você tiver uma versão desatualizada ou precisar instalar o PowerShell, confira [Instalando várias versões do PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6). As informações de instalação para sua plataforma estão vinculadas a partir dessa página.

## <a name="install-the-azure-powershell-module"></a>Instalar módulo do Azure PowerShell

> [!IMPORTANT]
>
> Você não deve ter ambos os módulos `AzureRM` e `Az` instalados em um sistema ao mesmo tempo. Para instalar o módulo `Az`, `AzureRM` deve ser desinstalado. Para obter instruções sobre como fazer isso, confira [Desinstalar o módulo Azure PowerShell (AzureRM)](uninstall-azurerm-ps.md).

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

Para começar a trabalhar com o Azure PowerShell, você precisa carregar `Az` em sua sessão atual do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar. A importação automática do módulo `Az` requer a configuração de um perfil do PowerShell. Saiba mais sobre isso em [Sobre Perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).
Para aprender a manter sua entrada no Azure entre as sessões, consulte [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).

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

Você pode carregar uma versão específica do módulo `Az` usando o argumento `-RequiredVersion` com `Install-Module` ou `Import-Module`:

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

Se você tiver mais de uma versão do módulo instalado, a versão mais recente é carregada, por padrão, durante a importação.

## <a name="provide-feedback"></a>Fornecer comentários

Se você encontrar um bug ao usar o Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).
Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.profile/send-feedback).

## <a name="next-steps"></a>Próximas etapas

Para começar a usar o Azure PowerShell, consulte [Introdução ao Azure PowerShell](get-started-azureps.md) para saber mais sobre o módulo e seus recursos.