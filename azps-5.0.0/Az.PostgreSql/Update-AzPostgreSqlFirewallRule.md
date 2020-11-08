---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118067"
---
# <span data-ttu-id="0238b-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0238b-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="0238b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0238b-102">SYNOPSIS</span></span>
<span data-ttu-id="0238b-103">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="0238b-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="0238b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0238b-104">SYNTAX</span></span>

### <span data-ttu-id="0238b-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="0238b-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0238b-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="0238b-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0238b-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0238b-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0238b-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0238b-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0238b-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0238b-109">DESCRIPTION</span></span>
<span data-ttu-id="0238b-110">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="0238b-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="0238b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0238b-111">EXAMPLES</span></span>

### <span data-ttu-id="0238b-112">Exemplo 1: atualizar a regra de firewall do PostgreSql por nome</span><span class="sxs-lookup"><span data-stu-id="0238b-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="0238b-113">Este cmdlet atualiza a regra de firewall PostgreSql por nome.</span><span class="sxs-lookup"><span data-stu-id="0238b-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="0238b-114">Exemplo 2: atualizar a regra de firewall do PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="0238b-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="0238b-115">Esses cmdlets atualizam a regra de firewall do PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="0238b-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="0238b-116">Exemplo 3: atualizar a regra de firewall do PostgreSql por-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="0238b-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="0238b-117">Esses cmdlets atualizam a regra de firewall do PostgreSql por-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="0238b-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="0238b-118">OS</span><span class="sxs-lookup"><span data-stu-id="0238b-118">PARAMETERS</span></span>

### <span data-ttu-id="0238b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0238b-119">-AsJob</span></span>
<span data-ttu-id="0238b-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="0238b-120">Run the command as a job</span></span>

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

### <span data-ttu-id="0238b-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="0238b-121">-ClientIPAddress</span></span>
<span data-ttu-id="0238b-122">Único IP especificado pelo cliente da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="0238b-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="0238b-123">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="0238b-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0238b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0238b-124">-DefaultProfile</span></span>
<span data-ttu-id="0238b-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0238b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0238b-126">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="0238b-126">-EndIPAddress</span></span>
<span data-ttu-id="0238b-127">O endereço IP final da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="0238b-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="0238b-128">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="0238b-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0238b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0238b-129">-InputObject</span></span>
<span data-ttu-id="0238b-130">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0238b-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0238b-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="0238b-131">-Name</span></span>
<span data-ttu-id="0238b-132">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="0238b-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="0238b-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0238b-133">-NoWait</span></span>
<span data-ttu-id="0238b-134">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="0238b-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0238b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0238b-135">-ResourceGroupName</span></span>
<span data-ttu-id="0238b-136">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0238b-136">The name of the resource group.</span></span>
<span data-ttu-id="0238b-137">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0238b-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0238b-138">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="0238b-138">-ServerName</span></span>
<span data-ttu-id="0238b-139">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="0238b-139">The name of the server.</span></span>

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

### <span data-ttu-id="0238b-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="0238b-140">-StartIPAddress</span></span>
<span data-ttu-id="0238b-141">O endereço IP inicial da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="0238b-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="0238b-142">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="0238b-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0238b-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0238b-143">-SubscriptionId</span></span>
<span data-ttu-id="0238b-144">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="0238b-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0238b-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0238b-145">-Confirm</span></span>
<span data-ttu-id="0238b-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0238b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0238b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0238b-147">-WhatIf</span></span>
<span data-ttu-id="0238b-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0238b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0238b-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0238b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0238b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0238b-150">CommonParameters</span></span>
<span data-ttu-id="0238b-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0238b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0238b-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0238b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0238b-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0238b-153">INPUTS</span></span>

### <span data-ttu-id="0238b-154">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0238b-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="0238b-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0238b-155">OUTPUTS</span></span>

### <span data-ttu-id="0238b-156">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0238b-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="0238b-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0238b-157">NOTES</span></span>

<span data-ttu-id="0238b-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0238b-158">ALIASES</span></span>

<span data-ttu-id="0238b-159">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="0238b-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0238b-160">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="0238b-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0238b-161">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0238b-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0238b-162">INPUTobject <IPostgreSqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="0238b-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0238b-163">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="0238b-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0238b-164">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0238b-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0238b-165">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="0238b-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0238b-166">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="0238b-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0238b-167">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="0238b-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0238b-168">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0238b-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0238b-169">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0238b-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="0238b-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="0238b-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0238b-171">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="0238b-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0238b-172">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="0238b-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0238b-173">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0238b-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0238b-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0238b-174">RELATED LINKS</span></span>

