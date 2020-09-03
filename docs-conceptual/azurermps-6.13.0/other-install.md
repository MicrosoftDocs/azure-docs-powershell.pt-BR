---
title: Outras maneiras de instalar o Azure PowerShell
description: Como instalar o Azure PowerShell sem o PowerShellGet usando uma MSI
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 41edefe96ecebf0a7276cdc3b4510acd7e8098f4
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241587"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Instalar o Azure PowerShell no Windows com a MSI

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

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
