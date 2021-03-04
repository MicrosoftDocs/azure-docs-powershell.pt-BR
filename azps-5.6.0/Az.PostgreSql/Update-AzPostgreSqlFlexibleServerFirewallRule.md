---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 26f6da2cdbf7d12e4d4927fd14ffc6b58b539bef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888217"
---
# <span data-ttu-id="d2453-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d2453-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="d2453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2453-102">SYNOPSIS</span></span>
<span data-ttu-id="d2453-103">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="d2453-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d2453-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d2453-104">SYNTAX</span></span>

### <span data-ttu-id="d2453-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d2453-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2453-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d2453-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2453-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d2453-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2453-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d2453-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d2453-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d2453-109">DESCRIPTION</span></span>
<span data-ttu-id="d2453-110">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="d2453-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d2453-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2453-111">EXAMPLES</span></span>

### <span data-ttu-id="d2453-112">Exemplo 1: Atualizar Regra de Firewall PostgreSql pelo nome</span><span class="sxs-lookup"><span data-stu-id="d2453-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="d2453-113">Este cmdlet atualiza a Regra de Firewall PostgreSql pelo nome.</span><span class="sxs-lookup"><span data-stu-id="d2453-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="d2453-114">Exemplo 2: Atualizar a Regra de Firewall PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="d2453-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="d2453-115">Esses cmdlets atualizem a Regra de Firewall PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="d2453-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="d2453-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d2453-116">PARAMETERS</span></span>

### <span data-ttu-id="d2453-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2453-117">-AsJob</span></span>
<span data-ttu-id="d2453-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="d2453-118">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2453-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d2453-119">-ClientIPAddress</span></span>
<span data-ttu-id="d2453-120">IP único especificado pelo cliente da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2453-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="d2453-121">Deve ser formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="d2453-121">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, ClientIPAddressViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2453-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2453-122">-DefaultProfile</span></span>
<span data-ttu-id="d2453-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2453-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2453-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="d2453-124">-EndIPAddress</span></span>
<span data-ttu-id="d2453-125">O endereço IP final da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2453-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="d2453-126">Deve ser formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="d2453-126">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2453-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2453-127">-InputObject</span></span>
<span data-ttu-id="d2453-128">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d2453-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2453-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d2453-129">-Name</span></span>
<span data-ttu-id="d2453-130">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2453-130">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2453-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d2453-131">-NoWait</span></span>
<span data-ttu-id="d2453-132">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="d2453-132">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2453-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2453-133">-ResourceGroupName</span></span>
<span data-ttu-id="d2453-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2453-134">The name of the resource group.</span></span>
<span data-ttu-id="d2453-135">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d2453-135">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2453-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d2453-136">-ServerName</span></span>
<span data-ttu-id="d2453-137">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2453-137">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2453-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="d2453-138">-StartIPAddress</span></span>
<span data-ttu-id="d2453-139">O endereço IP inicial da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2453-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="d2453-140">Deve ser formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="d2453-140">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2453-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2453-141">-SubscriptionId</span></span>
<span data-ttu-id="d2453-142">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d2453-142">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2453-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2453-143">-Confirm</span></span>
<span data-ttu-id="d2453-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2453-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2453-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2453-145">-WhatIf</span></span>
<span data-ttu-id="d2453-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2453-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2453-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2453-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2453-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2453-148">CommonParameters</span></span>
<span data-ttu-id="d2453-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2453-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2453-150">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2453-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2453-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2453-151">INPUTS</span></span>

### <span data-ttu-id="d2453-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d2453-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="d2453-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d2453-153">OUTPUTS</span></span>

### <span data-ttu-id="d2453-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d2453-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="d2453-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="d2453-155">NOTES</span></span>

<span data-ttu-id="d2453-156">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d2453-156">ALIASES</span></span>

<span data-ttu-id="d2453-157">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="d2453-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2453-158">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d2453-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2453-159">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d2453-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2453-160">INPUTOBJECT <IPostgreSqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="d2453-160">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2453-161">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2453-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d2453-162">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d2453-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d2453-163">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2453-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d2453-164">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d2453-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2453-165">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="d2453-165">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d2453-166">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2453-166">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d2453-167">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d2453-167">The name is case insensitive.</span></span>
  - <span data-ttu-id="d2453-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="d2453-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d2453-169">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2453-169">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d2453-170">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d2453-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d2453-171">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d2453-171">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d2453-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2453-172">RELATED LINKS</span></span>

