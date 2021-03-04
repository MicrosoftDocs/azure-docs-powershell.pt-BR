---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 1c7b3c1f64637554745e960fadfe93cb3d87fa84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890833"
---
# <span data-ttu-id="5e6f3-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5e6f3-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="5e6f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="5e6f3-103">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="5e6f3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5e6f3-104">SYNTAX</span></span>

### <span data-ttu-id="5e6f3-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5e6f3-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5e6f3-106">Obter</span><span class="sxs-lookup"><span data-stu-id="5e6f3-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5e6f3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e6f3-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5e6f3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5e6f3-108">DESCRIPTION</span></span>
<span data-ttu-id="5e6f3-109">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="5e6f3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e6f3-110">EXAMPLES</span></span>

### <span data-ttu-id="5e6f3-111">Exemplo 1: listar todas as regras de firewall em um MariaDB</span><span class="sxs-lookup"><span data-stu-id="5e6f3-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="5e6f3-112">Este comando lista todas as regras de girewall em um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="5e6f3-113">Exemplo 2: Obter uma regra de firewall em um MariaDB</span><span class="sxs-lookup"><span data-stu-id="5e6f3-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="5e6f3-114">Este comando obtém uma regra de firewall em um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="5e6f3-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5e6f3-115">PARAMETERS</span></span>

### <span data-ttu-id="5e6f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e6f3-116">-DefaultProfile</span></span>
<span data-ttu-id="5e6f3-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e6f3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e6f3-118">-InputObject</span></span>
<span data-ttu-id="5e6f3-119">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5e6f3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5e6f3-120">-Name</span></span>
<span data-ttu-id="5e6f3-121">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-121">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="5e6f3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e6f3-122">-ResourceGroupName</span></span>
<span data-ttu-id="5e6f3-123">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5e6f3-124">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5e6f3-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5e6f3-125">-ServerName</span></span>
<span data-ttu-id="5e6f3-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-126">The name of the server.</span></span>

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

### <span data-ttu-id="5e6f3-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e6f3-127">-SubscriptionId</span></span>
<span data-ttu-id="5e6f3-128">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="5e6f3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e6f3-129">CommonParameters</span></span>
<span data-ttu-id="5e6f3-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e6f3-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e6f3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e6f3-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e6f3-132">INPUTS</span></span>

### <span data-ttu-id="5e6f3-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="5e6f3-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="5e6f3-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5e6f3-134">OUTPUTS</span></span>

### <span data-ttu-id="5e6f3-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5e6f3-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="5e6f3-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="5e6f3-136">NOTES</span></span>

<span data-ttu-id="5e6f3-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5e6f3-137">ALIASES</span></span>

<span data-ttu-id="5e6f3-138">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="5e6f3-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e6f3-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e6f3-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e6f3-141">INPUTOBJECT <IMariaDbIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="5e6f3-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e6f3-142">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5e6f3-143">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5e6f3-144">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5e6f3-145">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="5e6f3-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e6f3-146">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5e6f3-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="5e6f3-148">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="5e6f3-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5e6f3-150">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5e6f3-151">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="5e6f3-152">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5e6f3-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e6f3-153">RELATED LINKS</span></span>

