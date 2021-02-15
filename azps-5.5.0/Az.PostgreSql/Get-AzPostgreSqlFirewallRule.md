---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114061"
---
# <span data-ttu-id="a9c94-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a9c94-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="a9c94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9c94-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c94-103">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="a9c94-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="a9c94-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9c94-104">SYNTAX</span></span>

### <span data-ttu-id="a9c94-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a9c94-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a9c94-106">Obter</span><span class="sxs-lookup"><span data-stu-id="a9c94-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a9c94-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a9c94-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9c94-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9c94-108">DESCRIPTION</span></span>
<span data-ttu-id="a9c94-109">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="a9c94-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="a9c94-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a9c94-110">EXAMPLES</span></span>

### <span data-ttu-id="a9c94-111">Exemplo 1: Lista todas as Regras de Firewall no servidor PostgreSql especificado</span><span class="sxs-lookup"><span data-stu-id="a9c94-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="a9c94-112">Este cmdlet lista toda a Regra de Firewall no servidor PostgreSql especificado.</span><span class="sxs-lookup"><span data-stu-id="a9c94-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="a9c94-113">Exemplo 2: Obter Regra de Firewall por nome</span><span class="sxs-lookup"><span data-stu-id="a9c94-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="a9c94-114">Este cmdlet obtém a Regra de Firewall por nome.</span><span class="sxs-lookup"><span data-stu-id="a9c94-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="a9c94-115">Exemplo 3: Obter Regra de Firewall por identidade</span><span class="sxs-lookup"><span data-stu-id="a9c94-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="a9c94-116">Este cmdlet obtém a Regra de Firewall por identidade.</span><span class="sxs-lookup"><span data-stu-id="a9c94-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="a9c94-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9c94-117">PARAMETERS</span></span>

### <span data-ttu-id="a9c94-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c94-118">-DefaultProfile</span></span>
<span data-ttu-id="a9c94-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c94-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9c94-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9c94-120">-InputObject</span></span>
<span data-ttu-id="a9c94-121">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="a9c94-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a9c94-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9c94-122">-Name</span></span>
<span data-ttu-id="a9c94-123">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="a9c94-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="a9c94-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9c94-124">-ResourceGroupName</span></span>
<span data-ttu-id="a9c94-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9c94-125">The name of the resource group.</span></span>
<span data-ttu-id="a9c94-126">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a9c94-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a9c94-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a9c94-127">-ServerName</span></span>
<span data-ttu-id="a9c94-128">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a9c94-128">The name of the server.</span></span>

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

### <span data-ttu-id="a9c94-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9c94-129">-SubscriptionId</span></span>
<span data-ttu-id="a9c94-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a9c94-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a9c94-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c94-131">CommonParameters</span></span>
<span data-ttu-id="a9c94-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9c94-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c94-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9c94-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c94-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="a9c94-134">INPUTS</span></span>

### <span data-ttu-id="a9c94-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a9c94-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="a9c94-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="a9c94-136">OUTPUTS</span></span>

### <span data-ttu-id="a9c94-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a9c94-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="a9c94-138">Notas</span><span class="sxs-lookup"><span data-stu-id="a9c94-138">NOTES</span></span>

<span data-ttu-id="a9c94-139">Aliases</span><span class="sxs-lookup"><span data-stu-id="a9c94-139">ALIASES</span></span>

<span data-ttu-id="a9c94-140">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="a9c94-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a9c94-141">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a9c94-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a9c94-142">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a9c94-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a9c94-143">INPUTOBJECT: <IPostgreSqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="a9c94-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a9c94-144">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="a9c94-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a9c94-145">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a9c94-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a9c94-146">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="a9c94-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a9c94-147">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="a9c94-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a9c94-148">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="a9c94-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a9c94-149">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9c94-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a9c94-150">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a9c94-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="a9c94-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="a9c94-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a9c94-152">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a9c94-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a9c94-153">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a9c94-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a9c94-154">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a9c94-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a9c94-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9c94-155">RELATED LINKS</span></span>

