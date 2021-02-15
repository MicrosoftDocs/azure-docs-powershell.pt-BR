---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 2b2f52d8dc4f9e31a86b666b7ee81981fa6bd18c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114280"
---
# <span data-ttu-id="4060f-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4060f-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="4060f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4060f-102">SYNOPSIS</span></span>
<span data-ttu-id="4060f-103">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="4060f-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="4060f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4060f-104">SYNTAX</span></span>

### <span data-ttu-id="4060f-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4060f-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4060f-106">Obter</span><span class="sxs-lookup"><span data-stu-id="4060f-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4060f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4060f-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4060f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4060f-108">DESCRIPTION</span></span>
<span data-ttu-id="4060f-109">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="4060f-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="4060f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4060f-110">EXAMPLES</span></span>

### <span data-ttu-id="4060f-111">Exemplo 1: Listar todas as regras de firewall sob um MariaDB</span><span class="sxs-lookup"><span data-stu-id="4060f-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="4060f-112">Esse comando lista todas as regras de girewall sob um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="4060f-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="4060f-113">Exemplo 2: Obter uma regra de firewall sob um MariaDB</span><span class="sxs-lookup"><span data-stu-id="4060f-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="4060f-114">Esse comando obtém uma regra de firewall sob um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="4060f-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="4060f-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4060f-115">PARAMETERS</span></span>

### <span data-ttu-id="4060f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4060f-116">-DefaultProfile</span></span>
<span data-ttu-id="4060f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4060f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4060f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4060f-118">-InputObject</span></span>
<span data-ttu-id="4060f-119">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="4060f-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4060f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4060f-120">-Name</span></span>
<span data-ttu-id="4060f-121">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="4060f-121">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4060f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4060f-122">-ResourceGroupName</span></span>
<span data-ttu-id="4060f-123">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="4060f-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4060f-124">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="4060f-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4060f-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4060f-125">-ServerName</span></span>
<span data-ttu-id="4060f-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="4060f-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4060f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4060f-127">-SubscriptionId</span></span>
<span data-ttu-id="4060f-128">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="4060f-128">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4060f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4060f-129">CommonParameters</span></span>
<span data-ttu-id="4060f-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4060f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4060f-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4060f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4060f-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="4060f-132">INPUTS</span></span>

### <span data-ttu-id="4060f-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="4060f-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="4060f-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="4060f-134">OUTPUTS</span></span>

### <span data-ttu-id="4060f-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4060f-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="4060f-136">Notas</span><span class="sxs-lookup"><span data-stu-id="4060f-136">NOTES</span></span>

<span data-ttu-id="4060f-137">Aliases</span><span class="sxs-lookup"><span data-stu-id="4060f-137">ALIASES</span></span>

<span data-ttu-id="4060f-138">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="4060f-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4060f-139">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4060f-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4060f-140">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4060f-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4060f-141">INPUTOBJECT: <IMariaDbIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="4060f-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4060f-142">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="4060f-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4060f-143">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4060f-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4060f-144">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="4060f-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4060f-145">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="4060f-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4060f-146">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="4060f-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4060f-147">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="4060f-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4060f-148">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="4060f-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4060f-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="4060f-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4060f-150">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="4060f-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4060f-151">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="4060f-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="4060f-152">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4060f-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4060f-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4060f-153">RELATED LINKS</span></span>

