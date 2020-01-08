---
title: Instalar o Azure PowerShell com um MSI
description: Como instalar o Azure PowerShell sem o PowerShellGet usando uma MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: d16aea3fa2059cd32f584134e2da43e01e3def31
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2020
ms.locfileid: "75721999"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Instalar o Azure PowerShell no Windows com a MSI

Este artigo explica como instalar o Azure PowerShell no Windows usando um instalador da MSI. O instalador do MSI (Microsoft Windows Installer) é fornecido para ambientes em que a Galeria do PowerShell pode ser bloqueada por um firewall ou em que um instalador offline é necessário. A maneira recomendada de instalar o Azure PowerShell é com o PowerShellGet. Para obter instruções sobre como usar o PowerShellGet para instalar o Azure PowerShell, confira [Instalar o Azure PowerShell com o PowerShellGet](install-az-ps.md).

## <a name="requirements"></a>Requisitos

O instalador MSI para Azure PowerShell funciona __somente__ para o PowerShell 5.1 no Windows. Para instalação em plataformas que não são Windows ou versões posteriores do PowerShell, [Instale com PowerShellGet](install-az-ps.md).
Para verificar sua versão do PowerShell, execute o comando:

```powershell-interactive
$PSVersionTable.PSVersion
```

Para usar o Azure PowerShell no PowerShell 5.1, é necessário:

1. Atualize para o [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) se necessário. Se você estiver usando o Windows 10, você já tem o PowerShell 5.1 instalado.
2. Instale o [.NET Framework 4.7.2 ou posterior](/dotnet/framework/install).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Instalar ou atualizar no Windows usando o pacote MSI

O Azure PowerShell para Windows é instalado usando o arquivo MSI disponível no [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v2.8.0-October2019). Se você tiver instalado versões anteriores dos módulos do Azure como um MSI, o instalador as removerá automaticamente. O pacote de MSI instala os módulos em `${env:ProgramFiles}\WindowsPowerShell\Modules`.

Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
>
> Se você desabilitou o carregamento automático do módulo, precisará importar manualmente o módulo com `Import-Module Az`. Por causa da maneira como o módulo está estruturado, isso pode levar até um minuto.

Será necessário repetir essa etapa para cada sessão nova do PowerShell que você iniciar. Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).

## <a name="provide-feedback"></a>Fornecer comentários

Se você encontrar um bug no Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).
Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Próximas etapas

Para saber mais sobre os módulos do Azure PowerShell e seus recursos, confira [Introdução ao Azure PowerShell](get-started-azureps.md).
Se você estiver familiarizado com o Azure PowerShell e precisar migrar do AzureRM, confira [Migrar do AzureRM para Az](migrate-from-azurerm-to-az.md).
