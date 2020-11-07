---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 2b2f52d8dc4f9e31a86b666b7ee81981fa6bd18c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955498"
---
# <span data-ttu-id="514a3-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="514a3-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="514a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="514a3-102">SYNOPSIS</span></span>
<span data-ttu-id="514a3-103">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="514a3-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="514a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="514a3-104">SYNTAX</span></span>

### <span data-ttu-id="514a3-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="514a3-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="514a3-106">Obter</span><span class="sxs-lookup"><span data-stu-id="514a3-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="514a3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="514a3-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="514a3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="514a3-108">DESCRIPTION</span></span>
<span data-ttu-id="514a3-109">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="514a3-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="514a3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="514a3-110">EXAMPLES</span></span>

### <span data-ttu-id="514a3-111">Exemplo 1: listar todas as regras de firewall em um MariaDB</span><span class="sxs-lookup"><span data-stu-id="514a3-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="514a3-112">Esse comando lista todas as regras girewall em um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="514a3-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="514a3-113">Exemplo 2: obter uma regra de firewall em um MariaDB</span><span class="sxs-lookup"><span data-stu-id="514a3-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="514a3-114">Esse comando obtém uma regra de firewall em um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="514a3-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="514a3-115">OS</span><span class="sxs-lookup"><span data-stu-id="514a3-115">PARAMETERS</span></span>

### <span data-ttu-id="514a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="514a3-116">-DefaultProfile</span></span>
<span data-ttu-id="514a3-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="514a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="514a3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="514a3-118">-InputObject</span></span>
<span data-ttu-id="514a3-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="514a3-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="514a3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="514a3-120">-Name</span></span>
<span data-ttu-id="514a3-121">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="514a3-121">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="514a3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="514a3-122">-ResourceGroupName</span></span>
<span data-ttu-id="514a3-123">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="514a3-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="514a3-124">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="514a3-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="514a3-125">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="514a3-125">-ServerName</span></span>
<span data-ttu-id="514a3-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="514a3-126">The name of the server.</span></span>

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

### <span data-ttu-id="514a3-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="514a3-127">-SubscriptionId</span></span>
<span data-ttu-id="514a3-128">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="514a3-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="514a3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="514a3-129">CommonParameters</span></span>
<span data-ttu-id="514a3-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="514a3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="514a3-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="514a3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="514a3-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="514a3-132">INPUTS</span></span>

### <span data-ttu-id="514a3-133">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="514a3-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="514a3-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="514a3-134">OUTPUTS</span></span>

### <span data-ttu-id="514a3-135">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="514a3-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="514a3-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="514a3-136">NOTES</span></span>

<span data-ttu-id="514a3-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="514a3-137">ALIASES</span></span>

<span data-ttu-id="514a3-138">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="514a3-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="514a3-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="514a3-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="514a3-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="514a3-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="514a3-141">INPUTobject <IMariaDbIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="514a3-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="514a3-142">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="514a3-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="514a3-143">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="514a3-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="514a3-144">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="514a3-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="514a3-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="514a3-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="514a3-146">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="514a3-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="514a3-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="514a3-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="514a3-148">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="514a3-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="514a3-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="514a3-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="514a3-150">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="514a3-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="514a3-151">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="514a3-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="514a3-152">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="514a3-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="514a3-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="514a3-153">RELATED LINKS</span></span>

