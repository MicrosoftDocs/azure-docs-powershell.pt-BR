---
title: Instale o Azure PowerShell no macOS ou no Linux
description: Como instalar o Azure PowerShell no macOS ou no Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 47611281f67d68c9fc2686e0c6156b060a225158
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587628"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Instale o Azure PowerShell no macOS ou no Linux

Para as plataformas não Windows, é possível executar o Azure PowerShell no PowerShell Core v6. Essa versão do PowerShell foi criada para usar em qualquer plataforma que dê suporte ao .NET Core. Para trabalhar com essas plataformas, há uma versão especial do .NET Core do Azure PowerShell disponível.

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

```powershell-interactive
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> O módulo `AzureRM` detalhado em outros artigos não foi compilado para o .NET Core e não funcionará com o PowerShell Core. `AzureRM` e `AzureRM.NetCore` usam os mesmos nomes de cmdlet, portanto a única diferença é o nome do módulo de rollup e para qual versão do .NET foram criados.

Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet. Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Responda `Yes` ou `Yes to All` para continuar a instalação.

## <a name="sign-in"></a>Entrar

Para começar a trabalhar com o Azure PowerShell, você precisa carregar `AzureRM.Netcore` em sua sessão do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure. __Não__ é necessário ter privilégios elevados para importar um módulo.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar. A importação automática do módulo `AzureRM` requer a configuração de um perfil do PowerShell. Saiba mais sobre isso em [Sobre Perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).
No macOS e no Linux, trabalhe com seu perfil usando a variável de ambiente `$Profile`. Para aprender a manter sua entrada no Azure entre as sessões, consulte [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).

## <a name="available-cmdlets"></a>Cmdlets disponíveis

Os módulos do Azure PowerShell para .NET Core ainda estão em desenvolvimento. Esses módulos não fornecem o conjunto completo de cmdlets que estão disponíveis para a versão do Windows dos módulos. As funções a seguir são implementadas em módulos AzureRM.Netcore:

* Gerenciamento de contas
  * Entrar com a conta da Microsoft, conta Organizacional ou Entidade de Serviço por meio do Microsoft Azure Active Directory
  * Salvar credenciais para o disco com Save-AzureRmContext e carregar as credenciais salvas usando Import-AzureRmContext
* Ambiente
  * Obter os diferentes ambientes do Microsoft Azure prontos para uso
  * Adicionar/definir/remover ambientes personalizados (como seus ambientes do Azure Stack ou do Pacote do Microsoft Azure)
* Cmdlets de plano de gerenciamento para os Serviços do Azure usando as interfaces do Resource Manager e do Gerenciamento de Serviços.
  * Máquina Virtual
  * Serviço de Aplicativo (Sites)
  * Banco de dados SQL
  * Armazenamento
  * Rede

## <a name="next-steps"></a>Próximas etapas

Para saber mais sobre como usar o Azure PowerShell, confira o artigo [Introdução ao Azure PowerShell](get-started-azureps.md).
