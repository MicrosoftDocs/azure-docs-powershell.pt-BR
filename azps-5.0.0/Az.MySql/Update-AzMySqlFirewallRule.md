---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: 979fc45bb7bdfe36133404a88a646a871cb33301
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125330"
---
# <span data-ttu-id="1e6ae-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1e6ae-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="1e6ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e6ae-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6ae-103">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="1e6ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e6ae-104">SYNTAX</span></span>

### <span data-ttu-id="1e6ae-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="1e6ae-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1e6ae-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="1e6ae-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1e6ae-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1e6ae-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1e6ae-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1e6ae-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1e6ae-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e6ae-109">DESCRIPTION</span></span>
<span data-ttu-id="1e6ae-110">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="1e6ae-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e6ae-111">EXAMPLES</span></span>

### <span data-ttu-id="1e6ae-112">Exemplo 1: atualizar a regra de firewall do MySql por nome</span><span class="sxs-lookup"><span data-stu-id="1e6ae-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="1e6ae-113">Este cmdlet atualiza a regra de firewall do MySql por nome.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="1e6ae-114">Exemplo 2: atualizar a regra de firewall do MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="1e6ae-115">Esses cmdlets atualizam a regra de firewall do MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="1e6ae-116">Exemplo 3: atualizar a regra de firewall do MySql por-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="1e6ae-117">Esses cmdlets atualizam a regra de firewall do MySql por-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="1e6ae-118">OS</span><span class="sxs-lookup"><span data-stu-id="1e6ae-118">PARAMETERS</span></span>

### <span data-ttu-id="1e6ae-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e6ae-119">-AsJob</span></span>
<span data-ttu-id="1e6ae-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="1e6ae-120">Run the command as a job</span></span>

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

### <span data-ttu-id="1e6ae-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="1e6ae-121">-ClientIPAddress</span></span>
<span data-ttu-id="1e6ae-122">Único IP especificado pelo cliente da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="1e6ae-123">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="1e6ae-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6ae-124">-DefaultProfile</span></span>
<span data-ttu-id="1e6ae-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e6ae-126">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="1e6ae-126">-EndIPAddress</span></span>
<span data-ttu-id="1e6ae-127">O endereço IP final da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="1e6ae-128">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="1e6ae-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e6ae-129">-InputObject</span></span>
<span data-ttu-id="1e6ae-130">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1e6ae-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e6ae-131">-Name</span></span>
<span data-ttu-id="1e6ae-132">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="1e6ae-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1e6ae-133">-NoWait</span></span>
<span data-ttu-id="1e6ae-134">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="1e6ae-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1e6ae-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e6ae-135">-ResourceGroupName</span></span>
<span data-ttu-id="1e6ae-136">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-136">The name of the resource group.</span></span>
<span data-ttu-id="1e6ae-137">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1e6ae-138">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="1e6ae-138">-ServerName</span></span>
<span data-ttu-id="1e6ae-139">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-139">The name of the server.</span></span>

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

### <span data-ttu-id="1e6ae-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="1e6ae-140">-StartIPAddress</span></span>
<span data-ttu-id="1e6ae-141">O endereço IP inicial da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="1e6ae-142">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="1e6ae-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e6ae-143">-SubscriptionId</span></span>
<span data-ttu-id="1e6ae-144">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1e6ae-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1e6ae-145">-Confirm</span></span>
<span data-ttu-id="1e6ae-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e6ae-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e6ae-147">-WhatIf</span></span>
<span data-ttu-id="1e6ae-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e6ae-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e6ae-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6ae-150">CommonParameters</span></span>
<span data-ttu-id="1e6ae-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6ae-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e6ae-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6ae-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e6ae-153">INPUTS</span></span>

### <span data-ttu-id="1e6ae-154">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="1e6ae-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="1e6ae-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e6ae-155">OUTPUTS</span></span>

### <span data-ttu-id="1e6ae-156">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1e6ae-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="1e6ae-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e6ae-157">NOTES</span></span>

<span data-ttu-id="1e6ae-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1e6ae-158">ALIASES</span></span>

<span data-ttu-id="1e6ae-159">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="1e6ae-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1e6ae-160">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1e6ae-161">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1e6ae-162">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="1e6ae-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1e6ae-163">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1e6ae-164">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1e6ae-165">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1e6ae-166">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="1e6ae-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1e6ae-167">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1e6ae-168">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1e6ae-169">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="1e6ae-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1e6ae-171">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1e6ae-172">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1e6ae-173">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="1e6ae-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1e6ae-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e6ae-174">RELATED LINKS</span></span>

