---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271646"
---
# <span data-ttu-id="f110b-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f110b-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="f110b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f110b-102">SYNOPSIS</span></span>
<span data-ttu-id="f110b-103">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="f110b-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="f110b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f110b-104">SYNTAX</span></span>

### <span data-ttu-id="f110b-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="f110b-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f110b-106">Obter</span><span class="sxs-lookup"><span data-stu-id="f110b-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f110b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f110b-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f110b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f110b-108">DESCRIPTION</span></span>
<span data-ttu-id="f110b-109">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="f110b-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="f110b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f110b-110">EXAMPLES</span></span>

### <span data-ttu-id="f110b-111">Exemplo 1: lista todas as regras de firewall no servidor PostgreSql especificado</span><span class="sxs-lookup"><span data-stu-id="f110b-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="f110b-112">Esse cmdlet lista todas as regras de firewall no servidor PostgreSql especificado.</span><span class="sxs-lookup"><span data-stu-id="f110b-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="f110b-113">Exemplo 2: obter a regra de firewall por nome</span><span class="sxs-lookup"><span data-stu-id="f110b-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="f110b-114">Este cmdlet obtém a regra de firewall por nome.</span><span class="sxs-lookup"><span data-stu-id="f110b-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="f110b-115">Exemplo 3: obter a regra de firewall por identidade</span><span class="sxs-lookup"><span data-stu-id="f110b-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="f110b-116">Este cmdlet obtém a regra de firewall por identidade.</span><span class="sxs-lookup"><span data-stu-id="f110b-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="f110b-117">OS</span><span class="sxs-lookup"><span data-stu-id="f110b-117">PARAMETERS</span></span>

### <span data-ttu-id="f110b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f110b-118">-DefaultProfile</span></span>
<span data-ttu-id="f110b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f110b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f110b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f110b-120">-InputObject</span></span>
<span data-ttu-id="f110b-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f110b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f110b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f110b-122">-Name</span></span>
<span data-ttu-id="f110b-123">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="f110b-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="f110b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f110b-124">-ResourceGroupName</span></span>
<span data-ttu-id="f110b-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f110b-125">The name of the resource group.</span></span>
<span data-ttu-id="f110b-126">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f110b-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f110b-127">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f110b-127">-ServerName</span></span>
<span data-ttu-id="f110b-128">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="f110b-128">The name of the server.</span></span>

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

### <span data-ttu-id="f110b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f110b-129">-SubscriptionId</span></span>
<span data-ttu-id="f110b-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f110b-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f110b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f110b-131">CommonParameters</span></span>
<span data-ttu-id="f110b-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f110b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f110b-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f110b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f110b-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f110b-134">INPUTS</span></span>

### <span data-ttu-id="f110b-135">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f110b-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="f110b-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f110b-136">OUTPUTS</span></span>

### <span data-ttu-id="f110b-137">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f110b-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="f110b-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f110b-138">NOTES</span></span>

<span data-ttu-id="f110b-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f110b-139">ALIASES</span></span>

<span data-ttu-id="f110b-140">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="f110b-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f110b-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f110b-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f110b-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f110b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f110b-143">INPUTobject <IPostgreSqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f110b-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f110b-144">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="f110b-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f110b-145">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f110b-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f110b-146">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="f110b-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f110b-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f110b-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f110b-148">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="f110b-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f110b-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f110b-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f110b-150">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f110b-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="f110b-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="f110b-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f110b-152">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="f110b-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f110b-153">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f110b-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f110b-154">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f110b-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f110b-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f110b-155">RELATED LINKS</span></span>

