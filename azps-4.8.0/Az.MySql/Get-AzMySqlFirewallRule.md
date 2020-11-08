---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
ms.openlocfilehash: 11278c1d317f6f4e0171513a4503c5681506f1ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113478"
---
# <span data-ttu-id="dc37d-101">Get-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dc37d-101">Get-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="dc37d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc37d-102">SYNOPSIS</span></span>
<span data-ttu-id="dc37d-103">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="dc37d-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="dc37d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc37d-104">SYNTAX</span></span>

### <span data-ttu-id="dc37d-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="dc37d-105">List (Default)</span></span>
```
Get-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc37d-106">Obter</span><span class="sxs-lookup"><span data-stu-id="dc37d-106">Get</span></span>
```
Get-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc37d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dc37d-107">GetViaIdentity</span></span>
```
Get-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dc37d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc37d-108">DESCRIPTION</span></span>
<span data-ttu-id="dc37d-109">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="dc37d-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="dc37d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc37d-110">EXAMPLES</span></span>

### <span data-ttu-id="dc37d-111">Exemplo 1: lista todas as regras de firewall no servidor MySql especificado</span><span class="sxs-lookup"><span data-stu-id="dc37d-111">Example 1: Lists all the Firewall Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="dc37d-112">Esse cmdlet lista todas as regras de firewall no servidor MySql especificado.</span><span class="sxs-lookup"><span data-stu-id="dc37d-112">This cmdlet lists all the Firewall Rule in specified MySql server.</span></span>

### <span data-ttu-id="dc37d-113">Exemplo 2: obter a regra de firewall por nome</span><span class="sxs-lookup"><span data-stu-id="dc37d-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="dc37d-114">Este cmdlet obtém a regra de firewall por nome.</span><span class="sxs-lookup"><span data-stu-id="dc37d-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="dc37d-115">Exemplo 3: obter a regra de firewall por identidade</span><span class="sxs-lookup"><span data-stu-id="dc37d-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Get-AzMySqlFirewallRule -InputObject $ID

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="dc37d-116">Este cmdlet obtém a regra de firewall por identidade.</span><span class="sxs-lookup"><span data-stu-id="dc37d-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="dc37d-117">OS</span><span class="sxs-lookup"><span data-stu-id="dc37d-117">PARAMETERS</span></span>

### <span data-ttu-id="dc37d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc37d-118">-DefaultProfile</span></span>
<span data-ttu-id="dc37d-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc37d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc37d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc37d-120">-InputObject</span></span>
<span data-ttu-id="dc37d-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="dc37d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc37d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc37d-122">-Name</span></span>
<span data-ttu-id="dc37d-123">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="dc37d-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="dc37d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc37d-124">-ResourceGroupName</span></span>
<span data-ttu-id="dc37d-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc37d-125">The name of the resource group.</span></span>
<span data-ttu-id="dc37d-126">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="dc37d-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dc37d-127">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="dc37d-127">-ServerName</span></span>
<span data-ttu-id="dc37d-128">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="dc37d-128">The name of the server.</span></span>

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

### <span data-ttu-id="dc37d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc37d-129">-SubscriptionId</span></span>
<span data-ttu-id="dc37d-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="dc37d-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dc37d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc37d-131">CommonParameters</span></span>
<span data-ttu-id="dc37d-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc37d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc37d-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc37d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc37d-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc37d-134">INPUTS</span></span>

### <span data-ttu-id="dc37d-135">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="dc37d-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="dc37d-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc37d-136">OUTPUTS</span></span>

### <span data-ttu-id="dc37d-137">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dc37d-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="dc37d-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc37d-138">NOTES</span></span>

<span data-ttu-id="dc37d-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dc37d-139">ALIASES</span></span>

<span data-ttu-id="dc37d-140">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="dc37d-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dc37d-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="dc37d-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc37d-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dc37d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dc37d-143">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="dc37d-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dc37d-144">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="dc37d-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="dc37d-145">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="dc37d-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="dc37d-146">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="dc37d-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="dc37d-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="dc37d-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc37d-148">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="dc37d-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="dc37d-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc37d-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dc37d-150">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="dc37d-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="dc37d-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="dc37d-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="dc37d-152">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="dc37d-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="dc37d-153">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="dc37d-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dc37d-154">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="dc37d-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="dc37d-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc37d-155">RELATED LINKS</span></span>

