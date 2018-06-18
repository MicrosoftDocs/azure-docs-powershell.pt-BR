---
title: Instalar o Azure PowerShell com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323094"
---
# <a name="install-azure-powershell-with-powershellget"></a>Instalar o Azure PowerShell com o PowerShellGet

Este artigo explica as etapas para instalar os módulos do Azure PowerShell em um ambiente Windows usando o PowerShellGet.  Este é o modo preferencial para instalar o Azure PowerShell, mas se você preferir instalar com o pacote do Web Platform Installer ou MSI, confira [Outros métodos de instalação](other-install.md).

Se você quiser usar o Azure PowerShell em macOS ou Linux, consulte o seguinte artigo: [Instalar e configurar o Azure PowerShell em macOS e Linux](install-azurermps-maclinux.md).

## <a name="system-requirements"></a>Requisitos do sistema

A versão 6.1.0 do Azure PowerShell requer a versão 5.0 (ou superior) do PowerShell. Para obter informações sobre como atualizar para o PowerShell 5.0, confira [Atualizações atuais do Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

O PowerShellGet é automaticamente incluído como parte do PowerShell 5.0.

## <a name="install-or-update-the-azure-powershell-module"></a>Instalar ou atualizar o módulo do Azure PowerShell

Instalando o Azure PowerShell a partir da Galeria do PowerShell requer privilégios elevados. Execute o comando a seguir em uma sessão do PowerShell com privilégios elevados:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> Este comando atualizará qualquer instalação existente do Azure PowerShell em seu sistema. Se você precisar ter mais de uma versão instalada, confira as respostas de Perguntas frequentes para [Posso instalar várias versões do Azure PowerShell?](#multiple-versions)

Por padrão, a Galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet. Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Responda “Sim” ou “Sim para Todos” para continuar com a instalação.

> [!NOTE]
> Caso sua versão seja mais antiga que a 2.8.5.201 do NuGet, será necessário baixar e instalar a versão mais recente do NuGet.

O AzureRM é um módulo do pacote cumulativo de atualizações para os cmdlets do Azure Resource Manager. Ao instalar o módulo AzureRM, qualquer outro módulo do Azure PowerShell que não tiver sido instalado anteriormente será baixado da Galeria do PowerShell.

## <a name="load-the-azure-powershell-module"></a>Carregar o módulo do Azure PowerShell

Depois de instalar o módulo, você precisa carregá-lo em sua sessão do PowerShell. Isso deve ser feito em uma sessão normal (não elevada) do PowerShell. Os módulos são carregados usando o cmdlet `Import-Module` da seguinte maneira:

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a>Relatando comentários e problemas

Se você encontrar quaisquer erros com a ferramenta, [relate um problema no GitHub](https://github.com/Azure/azure-powershell/issues). Para fornecer comentários na linha de comando, use o cmdlet `Send-Feedback`.

## <a name="next-steps"></a>Próximas etapas

Para obter mais informações sobre como usar o Azure PowerShell, consulte os seguintes artigos:

* [Introdução ao Azure PowerShell](get-started-azureps.md)

## <a name="frequently-asked-questions"></a>Perguntas frequentes

### <a id="helpmechoose"></a>Como posso verificar a versão do Azure PowerShell?

Embora recomendemos que você atualize para a última versão o mais cedo possível, várias versões do Azure PowerShell têm suporte. Para determinar a versão do Azure PowerShell instalada, execute `Get-Module AzureRM` na linha de comando.

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a>Posso usar o Azure PowerShell para implantações clássicas do Azure?

Se você tiver implantações que usam o modelo de implantação clássico, será possível instalar a versão de Gerenciamento de Serviços do Azure PowerShell. Para obter mais informações, veja [Instalar o módulo Gerenciamento de Serviços do Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps). Os módulos Azure e AzureRM compartilham dependências em comum. Caso você use ambos os módulos, Azure e AzureRM, instale a mesma versão de cada pacote.

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><a name="multiple-versions"/>Posso instalar várias versões do Azure PowerShell?

O PowerShellGet é o único método de instalação que oferece suporte a várias versões. Para instalar várias versões, você pode adicionar o parâmetro `-RequiredVersion` para o cmdlet `Install-Module`. Por exemplo, para instalar as duas versões 6.1.0 e 1.2.9:

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

somente uma versão do módulo pode ser carregada em uma sessão do PowerShell. Você deve abrir uma nova janela do PowerShell e usar `Import-Module` para importar uma versão específica do módulo do PowerShell.

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> A versão 2.1.0 e a versão 1.2.6 são as primeiras versões do módulo projetadas para ser instaladas e usadas lado a lado. Ao carregar uma versão anterior do Azure PowerShell, versões incompatíveis do módulo **AzureRM.Profile** serão carregadas. Desse modo, os cmdlets solicitarão que você faça logon sempre que um cmdlet for executado.
