---
title: Instale o Azure PowerShell no macOS ou no Linux
description: Como instalar o Azure PowerShell no macOS ou no Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: f014d62e898da195a38052db6b7e37a2cd96dfdd
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560109"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Instale o Azure PowerShell no macOS ou no Linux

Para as plataformas não Windows, é possível executar o Azure PowerShell no PowerShell Core v6. Essa versão do PowerShell foi criada para usar em qualquer plataforma que dê suporte ao .NET Core. Para trabalhar com essas plataformas, há uma versão do .NET Standard do Azure PowerShell disponível.

> [!NOTE]
> Atualmente, o PowerShell Core v6 e o Azure PowerShell para .NET Core ainda estão na versão beta.
> O suporte para esses produtos é limitado. Se você tiver problemas ou detectar erros, relate os problemas no GitHub.
>
> * [Problemas do PowerShell Core v6](https://github.com/PowerShell/PowerShell/issues)
> * [Problemas do Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>Instalar PowerShell Core

As instruções de instalação do PowerShell Core são diferentes para o macOS e a maioria das distribuições do Linux.
Instruções detalhadas podem ser encontradas nos seguintes artigos:

* [Instalar o PowerShell Core no macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [Instalar o PowerShell Core no Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>Instalar o Azure PowerShell para .NET Core

O PowerShell Core é fornecido com o módulo PowerShellGet já instalado. A instalação dos módulos no PowerShell requer privilégios elevados, portanto será necessário iniciar sua sessão como superusuário:

```bash
sudo pwsh
```

Para instalar o Azure PowerShell, execute o seguinte comando:

```powershell
Install-Module Az
```

> [!IMPORTANT]
> O módulo `AzureRM` detalhado em outros artigos não foi compilado para o .NET Core e não funcionará com o PowerShell Core. Os módulos `Az` contêm aliases de comando para todos os cmdlets `AzureRM` e, portanto, toda a documentação do `AzureRM` se aplica.

Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet. Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Responda `Yes` ou `Yes to All` para continuar a instalação.

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
