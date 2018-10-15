---
title: Instale o Azure PowerShell no macOS ou no Linux
description: Como instalar o Azure PowerShell no macOS ou no Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: c4f2bbd4bc9e2989549304493481f56cbbf5280a
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882041"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Instale o Azure PowerShell no macOS ou no Linux

Para as plataformas não Windows, é possível executar o Azure PowerShell no PowerShell Core v6. Essa versão do PowerShell foi criada para usar em qualquer plataforma que dê suporte ao .NET Core. Para trabalhar com essas plataformas, há uma versão do .NET Standard do Azure PowerShell disponível.

> [!NOTE]
> Neste momento, o Azure PowerShell para o .NET Standard ainda está na versão beta.
> Se você tiver problemas ou detectar erros, relate os problemas no GitHub.
>
> * [Problemas do Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>Instalar PowerShell Core

As instruções de instalação do PowerShell Core são diferentes para o macOS e a maioria das distribuições do Linux.
Instruções detalhadas podem ser encontradas nos seguintes artigos:

* [Instalar o PowerShell Core no macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [Instalar o PowerShell Core no Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a>Instalar o Azure PowerShell para .NET Standard

> [!IMPORTANT]
> O módulo `AzureRM` detalhado em outros artigos não funciona com o PowerShell Core.
> Você deve instalar o módulo `Az` para obter a funcionalidade do Azure PowerShell no PowerShell Core.

O PowerShell Core é fornecido com o módulo PowerShellGet já instalado. Inicie o PowerShell com o comando:

```bash
pwsh
```

Para instalar o Azure PowerShell, execute o seguinte comando:

```powershell
Install-Module Az
```

> [!NOTE]
> Se você encontrar um erro de permissões ao tentar instalar o módulo, precisará executar o PowerShell no modo de superusuário para instalar os módulos.
>
> ```bash
> sudo pwsh
> ```

Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet. Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Responda `Yes` ou `Yes to All` para continuar a instalação.

## <a name="enable-aliases"></a>Habilitar aliases

Para ter compatibilidade com o módulo `AzureRM`, o novo módulo `Az` é capaz de criar aliases compatíveis com versões anteriores para os cmdlets do `AzureRM`. Antes de usar o módulo pela primeira vez, configure esses aliases com o seguinte comando:

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

Isso configura aliases apenas para o usuário atual. Verifique a Ajuda do cmdlet para ver outros valores que podem ser fornecidos para `-Scope` a fim de configurar os aliases.

> [!NOTE]
> Se você encontrar um erro de localização de caminho, verifique se ele existe em seu sistema local. Para o escopo `CurrentUser`, esse erro pode ser resolvido executando o seguinte comando em `bash`:
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a>Entrar

Para começar a trabalhar com o Azure PowerShell, você precisa carregar `Az` em sua sessão do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure. __Não__ é necessário ter privilégios elevados para importar um módulo.

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar. A importação automática do módulo `Az` requer a configuração de um perfil do PowerShell. Saiba mais sobre isso em [Sobre Perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).
No macOS e no Linux, trabalhe com seu perfil usando a variável de ambiente `$Profile`. Para aprender a manter sua entrada no Azure entre as sessões, consulte [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).

## <a name="next-steps"></a>Próximas etapas

Para saber mais sobre como usar o Azure PowerShell, confira o artigo [Introdução ao Azure PowerShell](get-started-azureps.md).
