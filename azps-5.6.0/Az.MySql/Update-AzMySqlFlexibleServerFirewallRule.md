---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 2147921826c6f50882345bc68603b0dae8cb26ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887481"
---
# <span data-ttu-id="b3ba1-101">Update-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b3ba1-101">Update-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="b3ba1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ba1-103">Atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-103">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="b3ba1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b3ba1-104">SYNTAX</span></span>

### <span data-ttu-id="b3ba1-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b3ba1-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b3ba1-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b3ba1-106">ClientIPAddress</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b3ba1-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b3ba1-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b3ba1-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b3ba1-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b3ba1-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b3ba1-109">DESCRIPTION</span></span>
<span data-ttu-id="b3ba1-110">Atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-110">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="b3ba1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3ba1-111">EXAMPLES</span></span>

### <span data-ttu-id="b3ba1-112">Exemplo 1: Atualizar a Regra de Firewall mySql pelo nome</span><span class="sxs-lookup"><span data-stu-id="b3ba1-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="b3ba1-113">Este cmdlet atualiza a Regra de Firewall mySql pelo nome.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="b3ba1-114">Exemplo 2: Atualizar a Regra de Firewall mySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="b3ba1-115">Esses cmdlets atualizam a Regra de Firewall mySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="b3ba1-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b3ba1-116">PARAMETERS</span></span>

### <span data-ttu-id="b3ba1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3ba1-117">-AsJob</span></span>
<span data-ttu-id="b3ba1-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="b3ba1-118">Run the command as a job</span></span>

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

### <span data-ttu-id="b3ba1-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b3ba1-119">-ClientIPAddress</span></span>
<span data-ttu-id="b3ba1-120">IP único especificado pelo cliente da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="b3ba1-121">Deve ser formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b3ba1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ba1-122">-DefaultProfile</span></span>
<span data-ttu-id="b3ba1-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3ba1-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="b3ba1-124">-EndIPAddress</span></span>
<span data-ttu-id="b3ba1-125">O endereço IP final da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="b3ba1-126">Deve ser formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b3ba1-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3ba1-127">-InputObject</span></span>
<span data-ttu-id="b3ba1-128">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ba1-129">-Name</span><span class="sxs-lookup"><span data-stu-id="b3ba1-129">-Name</span></span>
<span data-ttu-id="b3ba1-130">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="b3ba1-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b3ba1-131">-NoWait</span></span>
<span data-ttu-id="b3ba1-132">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="b3ba1-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b3ba1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3ba1-133">-ResourceGroupName</span></span>
<span data-ttu-id="b3ba1-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-134">The name of the resource group.</span></span>
<span data-ttu-id="b3ba1-135">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b3ba1-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b3ba1-136">-ServerName</span></span>
<span data-ttu-id="b3ba1-137">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-137">The name of the server.</span></span>

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

### <span data-ttu-id="b3ba1-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="b3ba1-138">-StartIPAddress</span></span>
<span data-ttu-id="b3ba1-139">O endereço IP inicial da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="b3ba1-140">Deve ser formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b3ba1-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3ba1-141">-SubscriptionId</span></span>
<span data-ttu-id="b3ba1-142">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b3ba1-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3ba1-143">-Confirm</span></span>
<span data-ttu-id="b3ba1-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3ba1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3ba1-145">-WhatIf</span></span>
<span data-ttu-id="b3ba1-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3ba1-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3ba1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ba1-148">CommonParameters</span></span>
<span data-ttu-id="b3ba1-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ba1-150">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3ba1-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ba1-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3ba1-151">INPUTS</span></span>

### <span data-ttu-id="b3ba1-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b3ba1-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b3ba1-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b3ba1-153">OUTPUTS</span></span>

### <span data-ttu-id="b3ba1-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b3ba1-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="b3ba1-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="b3ba1-155">NOTES</span></span>

<span data-ttu-id="b3ba1-156">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b3ba1-156">ALIASES</span></span>

<span data-ttu-id="b3ba1-157">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="b3ba1-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b3ba1-158">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3ba1-159">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b3ba1-160">INPUTOBJECT <IMySqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="b3ba1-160">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b3ba1-161">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b3ba1-162">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b3ba1-163">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b3ba1-164">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b3ba1-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b3ba1-165">`[KeyName <String>]`: O nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-165">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="b3ba1-166">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-166">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b3ba1-167">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b3ba1-168">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="b3ba1-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b3ba1-170">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-170">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b3ba1-171">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-171">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b3ba1-172">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b3ba1-172">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b3ba1-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3ba1-173">RELATED LINKS</span></span>

