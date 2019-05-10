---
title: Outras maneiras de instalar o Azure PowerShell
description: Como instalar o Azure PowerShell sem o PowerShellGet usando uma MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 8fdf5598050cea2ef3f7422d53b22f9e49fe7477
ms.sourcegitcommit: b37b8bb6f8e39ecea5b50ceec48601eed313add7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65511665"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Instalar o Azure PowerShell no Windows com a MSI

Este artigo explica como instalar o Azure PowerShell no Windows usando um instalador da MSI.  
Use esses métodos de instalação somente se eles forem necessários para o seu sistema. A forma recomendada de Instalar o Azure PowerShell no Windows é com o PowerShellGet. Para obter instruções sobre como usar o PowerShellGet para instalar o Azure PowerShell, confira [Instalar o Azure PowerShell com o PowerShellGet](install-azurerm-ps.md).

> [!NOTE]
> O método Web Platform Installer da instalação não está mais disponível para as versões do Azure PowerShell 6.x e superior. Se você precisar usar o Web Platform Installer, considere usar a MSI ou pode instalar uma versão mais antiga do Azure PowerShell.

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Instalar ou atualizar no Windows usando o pacote MSI

O Azure PowerShell para o PowerShell do Windows 5.x pode ser instalado usando o arquivo MSI disponível no [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018). Se você tiver versões anteriores dos módulos do Azure instaladas como uma MSI, o instalador as removerá automaticamente. O pacote de MSI instala os módulos em `${env:ProgramFiles}\WindowsPowerShell\Modules`. Os módulos `AzureRM` e `Azure` são instalados.

> [!NOTE]
> Use o módulo `Azure` apenas se estiver trabalhando com o modelo de implantação clássico do Azure.

Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> Se você desabilitou o carregamento automático do módulo, precisará importar manualmente o módulo com `Import-Module AzureRM`. Por causa da maneira como o módulo está estruturado, isso pode levar alguns segundos.

Será necessário repetir essa etapa para cada sessão nova do PowerShell que você iniciar. Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).
