---
title: Instalar o Azure PowerShell com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 21345445efc89ab54bb7483cfe81f439f0a887a3
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861315"
---
# <a name="install-the-azure-powershell-module"></a>Instalar módulo do Azure PowerShell

Este artigo informa como instalar os módulos do Azure PowerShell usando o PowerShellGet. Essas instruções funcionam nas plataformas Windows, macOS e Linux. Para o módulo Az, atualmente não há suporte para outros métodos de instalação.

## <a name="requirements"></a>Requisitos

O Azure PowerShell funciona com o PowerShell 5.1 ou superior no Windows ou com o PowerShell Core 6.x e posterior em todas as plataformas. Se você não tiver certeza se tem o PowerShell ou se está no macOS ou no Linux, [instale a última versão do PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).

Para verificar sua versão do PowerShell, execute o comando:

```powershell-interactive
$PSVersionTable.PSVersion
```

Para executar o Azure PowerShell no PowerShell 5.1 no Windows:

1. Atualize para o [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) se necessário. Se você estiver usando o Windows 10, você já tem o PowerShell 5.1 instalado.
2. Instale o [.NET Framework 4.7.2 ou posterior](/dotnet/framework/install).

Não há nenhum requisito adicional para o Azure PowerShell ao usar o PowerShell Core.

## <a name="install-the-azure-powershell-module"></a>Instalar módulo do Azure PowerShell

> [!WARNING]
> __Não__ é possível instalar os módulos AzureRM e Az para o PowerShell 5.1 para Windows ao mesmo tempo. Caso você precise manter o AzureRM disponível no sistema, instale o módulo Az para o PowerShell Core 6.x ou posterior. Para fazer isso, [instale o PowerShell Core 6.x ou posterior](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) e, depois, siga estas instruções em um terminal do PowerShell Core.

O método de instalação recomendado deve apenas ser instalado para o usuário ativo:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Se desejar instalar para todos os usuários em um sistema, isso requererá privilégios de administrador. Em uma sessão do PowerShell com privilégios elevados executada como administrador ou com o comando `sudo` em macOS ou Linux:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
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

O módulo Az é um módulo de rollup para os cmdlets do Azure PowerShell. A instalação dele baixa todos os módulos disponíveis do Azure Resource Manager e possibilita usar seus cmdlets.

## <a name="troubleshooting"></a>solução de problemas

Estes são alguns problemas comuns observados durante a instalação do módulo do Azure PowerShell. Caso você tenha um problema que não foi listado aqui, [registre um problema no GitHub](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Conexão de blocos de proxy

Se você obtiver erros de `Install-Module` que indicam que a Galeria do PowerShell está inacessível, talvez você esteja protegido por um proxy. Sistemas operacionais diferentes terão requisitos diferentes para configurar um proxy de todo o sistema, que não são abordados detalhadamente aqui. Entre em contato com o administrador do sistema para obter as configurações de proxy e saber como defini-las para seu sistema operacional.

O PowerShell em si pode não ser configurado para usar esse proxy automaticamente. Com o PowerShell 5.1 e posterior, configure o proxy a ser usado para uma sessão do PowerShell com o seguinte comando:

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

Caso suas credenciais do sistema operacional estejam configuradas corretamente, isso roteará as solicitações do PowerShell por meio do proxy.
Para manter essa configuração entre as sessões, adicione o comando a um [perfil do PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).

Para instalar o pacote, o proxy precisa permitir conexões HTTPS para o seguinte endereço:

* `https://www.powershellgallery.com`

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

Devido ao modo de empacotamento do módulo Az, o comando [Update-Module](/powershell/module/powershellget/update-module) não atualizará a instalação corretamente. O Az é tecnicamente um metamódulo, abrangendo todos os submódulos que contêm cmdlets para interagir com os serviços do Azure. Isso significa que, para atualizar o módulo do Azure PowerShell, você precisará fazer uma __reinstalação__, em vez de apenas uma __atualização__. Isso é feito da mesma forma que a instalação, mas talvez você precise adicionar o argumento `-Force`:

```powershell
Install-Module -Name Az -AllowClobber -Force
```

Embora isso possa substituir os módulos instalados, você ainda poderá ter versões mais antigas no sistema.
Para saber como remover as versões antigas do Azure PowerShell do sistema, confira [Desinstalar o módulo do Azure PowerShell](uninstall-az-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Usar várias versões do Azure PowerShell

É possível instalar mais de uma versão do Azure PowerShell. Para verificar se você tem diversas versões do Azure PowerShell instaladas, use o seguinte comando:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

Para remover uma versão do Azure PowerShell, confira [Desinstalar módulo do Azure PowerShell](uninstall-az-ps.md).

Você pode instalar ou carregar uma versão específica do módulo `Az` usando o argumento `-RequiredVersion`:

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

Se você tiver mais de uma versão do módulo instalada, o carregamento automático do módulo e o `Import-Module` carregarão a versão mais recente por padrão.

## <a name="provide-feedback"></a>Fornecer comentários

Se você encontrar um bug no Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).
Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Próximas etapas

Para saber mais sobre os módulos do Azure PowerShell e seus recursos, confira [Introdução ao Azure PowerShell](get-started-azureps.md).
Se você estiver familiarizado com o Azure PowerShell e precisar migrar do AzureRM, confira [Migrar do AzureRM para Az](migrate-from-azurerm-to-az.md).
