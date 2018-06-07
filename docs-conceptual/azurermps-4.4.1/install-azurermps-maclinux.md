---
title: Instalar e configurar o Azure PowerShell em macOS e Linux | Microsoft Docs
description: Como instalar e configurar o Azure PowerShell para o primeiro uso em macOS e Linux.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 18f07d3eebcce74988a02b78f2cc85f7663ed225
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821897"
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a>Instalar e configurar o Azure PowerShell em macOS e Linux

Agora é possível instalar o PowerShell Core v6 e o Azure PowerShell em plataformas não Windows.
O processo de instalação do Azure PowerShell no macOS e Linux não é diferente do Windows, no entanto, você deve primeiro instalar PowerShell Core v6.

> [!NOTE]

> Atualmente, o PowerShell Core v6 e o Azure PowerShell para .NET Core ainda estão na versão beta.
> O suporte para esses produtos é limitado. Se você tiver problemas ou detectar erros, envie os problemas no GitHub.
>
> * [Problemas do PowerShell Core v6](https://github.com/PowerShell/PowerShell/issues)
> * [Problemas do Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a>Etapa 1: Instalar o PowerShell Core v6

O processo de instalação do PowerShell Core v6 varia dependendo do sistema operacional de destino.
Embora seja possível instalar o PowerShell Core v6 no Windows, este artigo concentra-se em macOS e Linux. Se você quiser usar o Azure PowerShell no Windows, consulte o artigo de [instalação](./install-azurerm-ps.md) para Windows.

A instalação do **PowerShell Core v6** no Linux ou no macOS varia de acordo com a distribuição de Linux e a versão do sistema operacional.
Instruções detalhadas podem ser encontradas no seguinte artigo:

- [Instalação do PowerShell Core no macOS e no Linux](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a>Etapa 2: instalar o Azure PowerShell para .NET Core

O PowerShell Core v6 é fornecido com o módulo PowerShellGet já instalado. Isso torna fácil instalar qualquer módulo que está publicado na Galeria do PowerShell. Para instalar o Azure PowerShell, abra uma nova sessão do PowerShell e execute o seguinte comando:

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a>Etapa 3: carregar o módulo AzureRM.Netcore

Depois de instalar o módulo, você precisa carregá-lo em sua sessão do PowerShell. Os módulos são carregados usando o cmdlet `Import-Module` da seguinte maneira:

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

Depois que a importação for concluída, você poderá testar seu módulo recém-instalado tentando entrar no Azure usando o seguinte comando:

```powershell
Login-AzureRMAccount
```

O comando acima solicitará que você acesse `https://aka.ms/devicelogin` e insira o código fornecido.

## <a name="available-cmdlets"></a>Cmdlets disponíveis

Os módulos do Azure PowerShell para .NET padrão ainda estão em desenvolvimento. Esses módulos não fornecem o conjunto completo de cmdlets que estão disponíveis para a versão do Windows dos módulos. As funções a seguir são implementadas em módulos AzureRM.Netcore:

* Gerenciamento de contas
  - Fazer logon com a conta da Microsoft, conta organizacional ou entidade de serviço por meio do Microsoft Azure Active Directory
  - Salvar credenciais para o disco com Save-AzureRmContext e carregar as credenciais salvas usando Import-AzureRmContext
* Ambiente
  - Obter os diferentes ambientes do Microsoft Azure prontos para uso
  - Adicionar/definir/remover ambientes personalizados (como seus ambientes do Azure Stack ou do Pacote do Microsoft Azure)
* Cmdlets de plano de gerenciamento para os Serviços do Azure usando as interfaces do Resource Manager e do Gerenciamento de Serviços.
  - Máquina Virtual
  - Serviço de Aplicativo (Sites)
  - Banco de dados SQL
  - Armazenamento
  - Rede

## <a name="next-steps"></a>Próximas etapas

Para saber mais sobre como usar o Azure PowerShell, confira o artigo [Introdução ao Azure PowerShell](get-started-azureps.md).
