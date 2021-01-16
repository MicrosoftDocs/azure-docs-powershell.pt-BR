---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 5df722564e899d46a1f68bf8e88ecdaa2b792121
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262653"
---
# <span data-ttu-id="b8c54-101">Update-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b8c54-101">Update-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="b8c54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8c54-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c54-103">Atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="b8c54-103">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="b8c54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8c54-104">SYNTAX</span></span>

### <span data-ttu-id="b8c54-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8c54-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b8c54-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b8c54-106">ClientIPAddress</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b8c54-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b8c54-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b8c54-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b8c54-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b8c54-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8c54-109">DESCRIPTION</span></span>
<span data-ttu-id="b8c54-110">Atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="b8c54-110">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="b8c54-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8c54-111">EXAMPLES</span></span>

### <span data-ttu-id="b8c54-112">Exemplo 1: atualizar a regra de firewall do MySql por nome</span><span class="sxs-lookup"><span data-stu-id="b8c54-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="b8c54-113">Este cmdlet atualiza a regra de firewall do MySql por nome.</span><span class="sxs-lookup"><span data-stu-id="b8c54-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="b8c54-114">Exemplo 2: atualizar a regra de firewall do MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="b8c54-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="b8c54-115">Esses cmdlets atualizam a regra de firewall do MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="b8c54-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="b8c54-116">OS</span><span class="sxs-lookup"><span data-stu-id="b8c54-116">PARAMETERS</span></span>

### <span data-ttu-id="b8c54-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8c54-117">-AsJob</span></span>
<span data-ttu-id="b8c54-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="b8c54-118">Run the command as a job</span></span>

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

### <span data-ttu-id="b8c54-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b8c54-119">-ClientIPAddress</span></span>
<span data-ttu-id="b8c54-120">Único IP especificado pelo cliente da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="b8c54-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="b8c54-121">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="b8c54-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b8c54-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c54-122">-DefaultProfile</span></span>
<span data-ttu-id="b8c54-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8c54-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8c54-124">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="b8c54-124">-EndIPAddress</span></span>
<span data-ttu-id="b8c54-125">O endereço IP final da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="b8c54-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="b8c54-126">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="b8c54-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b8c54-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8c54-127">-InputObject</span></span>
<span data-ttu-id="b8c54-128">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b8c54-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b8c54-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8c54-129">-Name</span></span>
<span data-ttu-id="b8c54-130">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="b8c54-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="b8c54-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b8c54-131">-NoWait</span></span>
<span data-ttu-id="b8c54-132">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="b8c54-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b8c54-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c54-133">-ResourceGroupName</span></span>
<span data-ttu-id="b8c54-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8c54-134">The name of the resource group.</span></span>
<span data-ttu-id="b8c54-135">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b8c54-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b8c54-136">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b8c54-136">-ServerName</span></span>
<span data-ttu-id="b8c54-137">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b8c54-137">The name of the server.</span></span>

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

### <span data-ttu-id="b8c54-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="b8c54-138">-StartIPAddress</span></span>
<span data-ttu-id="b8c54-139">O endereço IP inicial da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="b8c54-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="b8c54-140">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="b8c54-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b8c54-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8c54-141">-SubscriptionId</span></span>
<span data-ttu-id="b8c54-142">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b8c54-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b8c54-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b8c54-143">-Confirm</span></span>
<span data-ttu-id="b8c54-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8c54-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8c54-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c54-145">-WhatIf</span></span>
<span data-ttu-id="b8c54-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8c54-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8c54-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8c54-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8c54-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c54-148">CommonParameters</span></span>
<span data-ttu-id="b8c54-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c54-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c54-150">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8c54-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c54-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8c54-151">INPUTS</span></span>

### <span data-ttu-id="b8c54-152">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b8c54-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b8c54-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8c54-153">OUTPUTS</span></span>

### <span data-ttu-id="b8c54-154">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b8c54-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="b8c54-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8c54-155">NOTES</span></span>

<span data-ttu-id="b8c54-156">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b8c54-156">ALIASES</span></span>

<span data-ttu-id="b8c54-157">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="b8c54-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b8c54-158">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b8c54-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b8c54-159">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b8c54-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b8c54-160">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="b8c54-160">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b8c54-161">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="b8c54-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b8c54-162">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b8c54-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b8c54-163">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="b8c54-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b8c54-164">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b8c54-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b8c54-165">`[KeyName <String>]`: O nome da tecla do servidor.</span><span class="sxs-lookup"><span data-stu-id="b8c54-165">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="b8c54-166">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="b8c54-166">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b8c54-167">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8c54-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b8c54-168">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b8c54-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="b8c54-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="b8c54-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b8c54-170">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b8c54-170">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b8c54-171">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b8c54-171">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b8c54-172">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b8c54-172">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b8c54-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8c54-173">RELATED LINKS</span></span>

