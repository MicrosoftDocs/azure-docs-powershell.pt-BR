---
title: Introdução ao Azure PowerShell
description: Introdução ao Azure PowerShell
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 8958570285e3db264b3e0bb654acb7f38526354c
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93409798"
---
# <a name="get-started-with-azure-powershell"></a>Introdução ao Azure PowerShell

O Azure PowerShell foi projetado para gerenciar e administrar recursos do Azure na linha de comando. Use o Azure PowerShell quando quiser compilar ferramentas automatizadas que usam o modelo do Azure Resource Manager.
Teste-o em seu navegador com o [Azure Cloud Shell](/azure/cloud-shell/overview) ou instale-o em seu computador local.

Este artigo ajuda você a começar a usar o Azure PowerShell, além de ensinar os conceitos básicos por trás dele.

## <a name="install-or-run-in-azure-cloud-shell"></a>Instalar ou executar no Azure Cloud Shell

A maneira mais fácil para começar a usar o Azure PowerShell é testando-o em um ambiente do Azure Cloud Shell.
Para começar a usar o Cloud Shell, confira [Início Rápido do PowerShell no Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).
O Cloud Shell executa o PowerShell 6 em um contêiner do Linux, portanto, uma funcionalidade específica do Windows não está disponível.

Quando você estiver pronto para instalar o Azure PowerShell em seu computador local, siga as instruções em [Instalar o módulo do Azure PowerShell](install-az-ps.md).

## <a name="sign-in-to-azure"></a>Entrar no Azure

Entre interativamente com o cmdlet `Connect-AzAccount`. Caso use o Cloud Shell, ignore esta etapa: Sua sessão do Azure Cloud Shell já está autenticada para o ambiente, a assinatura e o locatário que iniciaram a sessão do Cloud Shell.

```azurepowershell-interactive
Connect-AzAccount
```

Se você estiver em uma região fora dos EUA, use o parâmetro `-Environment` para entrar. Obtenha o nome do ambiente para sua região usando o cmdlet [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment). Por exemplo, para entrar no Azure China 21Vianet:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Em ambientes do PowerShell 5.1, você receberá uma caixa de diálogo de entrada para fornecer um nome de usuário e uma senha de sua conta do Azure. Em todas as outras versões do PowerShell, você receberá um token para usá-lo em [https://microsoft.com/devicelogin ].
Abra essa página no seu navegador e insira o token, depois entre com suas credenciais da conta do Azure e autorize o Azure PowerShell.

Depois de entrar, você verá informações indicando qual das suas assinaturas do Azure está ativa. Caso você tenha várias assinaturas do Azure em sua conta e queira selecionar uma diferente, obtenha suas assinaturas disponíveis com o [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) e use o cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext) com sua ID da assinatura.
Para obter mais informações sobre como gerenciar suas assinaturas do Azure no Azure PowerShell, confira [Usar várias assinaturas do Azure](manage-subscriptions-azureps.md).

Depois de entrar, use os cmdlets do Azure PowerShell para acessar e gerenciar os recursos em sua assinatura. Para saber mais sobre o processo de entrada e os métodos de autenticação, confira [Entrar com o Azure PowerShell](authenticate-azureps.md).

## <a name="find-commands"></a>Localizar comandos

Os cmdlets do Azure PowerShell seguem uma convenção de nomenclatura padrão para o PowerShell, `VERB-NOUN`. O verbo descreve a ação (por exemplo, `New`, `Get`, `Set`, `Remove`) e o substantivo descreve o tipo de recurso (por exemplo, `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`). Os substantivos no Azure PowerShell sempre começam com o prefixo `Az`. Para obter a lista completa de verbos padrão, confira [Verbos aprovados para comandos do PowerShell](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).

Conhecer os substantivos, verbos e os módulos disponíveis do Azure PowerShell ajudará você a localizar os comandos com o cmdlet [Get-Command](/powershell/module/microsoft.powershell.core/get-command). Por exemplo, para localizar todos os comandos relacionados à VM que usam o verbo `Get`:

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

Para ajudar você a localizar os comandos comuns, esta tabela lista o tipo de recurso, o módulo correspondente do Azure PowerShell e o prefixo do substantivo para usar com `Get-Command`:

| Tipo de recurso | Módulo do Azure PowerShell | Prefixo do substantivo |
|---------------|-------------------------|----------------|
| [Grupo de recursos](/azure/azure-resource-manager/resource-group-overview) | [Az.Resources](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [Máquinas virtuais](/azure/virtual-machines) | [Az.Compute](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [Contas de armazenamento](/azure/storage/common/storage-introduction) | [Az.Storage](/powershell/module/az.storage/) | `AzStorageAccount` |
| [Key Vault](/azure/key-vault/key-vault-whatis) | [Az.KeyVault](/powershell/module/az.keyvault) | `AzKeyVault` |
| [Aplicativos Web](/azure/app-service) | [Az.Websites](/powershell/module/az.websites) | `AzWebApp` |
| [Bancos de dados SQL](/azure/sql-database) | [Az.Sql](/powershell/module/az.sql) | `AzSqlDatabase` |

Para obter uma lista completa dos módulos do Azure PowerShell, confira a [lista de módulos do PowerShell do Azure](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hospedada no GitHub.

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a>Aprenda as noções básicas do Azure PowerShell com guias de início rápido e tutoriais

Para começar a usar o Azure PowerShell, teste um tutorial aprofundado para configurar máquinas virtuais e aprender como consultá-las.

> [!div class="nextstepaction"]
> [Criar máquinas virtuais com o Azure PowerShell](azureps-vm-tutorial.yml)

Também há guias de início rápido do Azure PowerShell para outros serviços populares do Azure:

* [Criar uma conta de armazenamento](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [Transferir objetos de/para o armazenamento de Blobs do Azure](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [Criar e recuperar segredos do Azure Key Vault](/azure/key-vault/quick-create-powershell)
* [Criar um firewall e um banco de dados SQL do Azure](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [Executar um contêiner em Instâncias de Contêiner do Azure](/azure/container-instances/container-instances-quickstart-powershell)
* [Criar um VMSS (Conjunto de Dimensionamento de Máquina Virtual)](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [Criar um balanceador de carga padrão](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a>Próximas etapas

* [Entrar com o Azure PowerShell](authenticate-azureps.md)
* [Gerenciar as assinaturas do Azure com o Azure PowerShell](manage-subscriptions-azureps.md)
* [Criar entidades de serviço com o Azure PowerShell](create-azure-service-principal-azureps.md)
* Obtenha ajuda da comunidade:
  * [Fórum do Azure no MSDN](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Stack Overflow](https://go.microsoft.com/fwlink/?LinkId=320213)
