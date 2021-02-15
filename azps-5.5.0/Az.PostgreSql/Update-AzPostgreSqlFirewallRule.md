---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111486"
---
# <span data-ttu-id="df5e7-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="df5e7-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="df5e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="df5e7-103">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="df5e7-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="df5e7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df5e7-104">SYNTAX</span></span>

### <span data-ttu-id="df5e7-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="df5e7-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="df5e7-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="df5e7-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="df5e7-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="df5e7-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="df5e7-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="df5e7-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="df5e7-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="df5e7-109">DESCRIPTION</span></span>
<span data-ttu-id="df5e7-110">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="df5e7-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="df5e7-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="df5e7-111">EXAMPLES</span></span>

### <span data-ttu-id="df5e7-112">Exemplo 1: Atualizar Regra de Firewall PostgreSql por nome</span><span class="sxs-lookup"><span data-stu-id="df5e7-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="df5e7-113">Este cmdlet atualiza a Regra de Firewall PostgreSql por nome.</span><span class="sxs-lookup"><span data-stu-id="df5e7-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="df5e7-114">Exemplo 2: Atualizar a Regra de Firewall PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="df5e7-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="df5e7-115">Esses cmdlets atualizam a Regra de Firewall PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="df5e7-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="df5e7-116">Exemplo 3: Atualizar a Regra de Firewall PostgreSql por -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="df5e7-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="df5e7-117">Esses cmdlets atualizam a Regra de Firewall PostgreSql por -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="df5e7-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="df5e7-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df5e7-118">PARAMETERS</span></span>

### <span data-ttu-id="df5e7-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df5e7-119">-AsJob</span></span>
<span data-ttu-id="df5e7-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="df5e7-120">Run the command as a job</span></span>

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

### <span data-ttu-id="df5e7-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="df5e7-121">-ClientIPAddress</span></span>
<span data-ttu-id="df5e7-122">O cliente especificou um ÚNICO IP da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="df5e7-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="df5e7-123">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="df5e7-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="df5e7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df5e7-124">-DefaultProfile</span></span>
<span data-ttu-id="df5e7-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df5e7-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df5e7-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="df5e7-126">-EndIPAddress</span></span>
<span data-ttu-id="df5e7-127">O endereço IP final da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="df5e7-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="df5e7-128">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="df5e7-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="df5e7-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df5e7-129">-InputObject</span></span>
<span data-ttu-id="df5e7-130">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="df5e7-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="df5e7-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="df5e7-131">-Name</span></span>
<span data-ttu-id="df5e7-132">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="df5e7-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="df5e7-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="df5e7-133">-NoWait</span></span>
<span data-ttu-id="df5e7-134">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="df5e7-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="df5e7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df5e7-135">-ResourceGroupName</span></span>
<span data-ttu-id="df5e7-136">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df5e7-136">The name of the resource group.</span></span>
<span data-ttu-id="df5e7-137">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="df5e7-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="df5e7-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df5e7-138">-ServerName</span></span>
<span data-ttu-id="df5e7-139">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="df5e7-139">The name of the server.</span></span>

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

### <span data-ttu-id="df5e7-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="df5e7-140">-StartIPAddress</span></span>
<span data-ttu-id="df5e7-141">O endereço IP inicial da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="df5e7-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="df5e7-142">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="df5e7-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="df5e7-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df5e7-143">-SubscriptionId</span></span>
<span data-ttu-id="df5e7-144">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="df5e7-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="df5e7-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="df5e7-145">-Confirm</span></span>
<span data-ttu-id="df5e7-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df5e7-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df5e7-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df5e7-147">-WhatIf</span></span>
<span data-ttu-id="df5e7-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="df5e7-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df5e7-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df5e7-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df5e7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df5e7-150">CommonParameters</span></span>
<span data-ttu-id="df5e7-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df5e7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df5e7-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df5e7-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df5e7-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="df5e7-153">INPUTS</span></span>

### <span data-ttu-id="df5e7-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="df5e7-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="df5e7-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="df5e7-155">OUTPUTS</span></span>

### <span data-ttu-id="df5e7-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="df5e7-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="df5e7-157">Notas</span><span class="sxs-lookup"><span data-stu-id="df5e7-157">NOTES</span></span>

<span data-ttu-id="df5e7-158">Aliases</span><span class="sxs-lookup"><span data-stu-id="df5e7-158">ALIASES</span></span>

<span data-ttu-id="df5e7-159">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="df5e7-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="df5e7-160">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="df5e7-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="df5e7-161">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="df5e7-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="df5e7-162">INPUTOBJECT: <IPostgreSqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="df5e7-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="df5e7-163">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="df5e7-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="df5e7-164">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="df5e7-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="df5e7-165">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="df5e7-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="df5e7-166">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="df5e7-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="df5e7-167">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="df5e7-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="df5e7-168">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df5e7-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="df5e7-169">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="df5e7-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="df5e7-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="df5e7-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="df5e7-171">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="df5e7-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="df5e7-172">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="df5e7-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="df5e7-173">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="df5e7-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="df5e7-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df5e7-174">RELATED LINKS</span></span>

