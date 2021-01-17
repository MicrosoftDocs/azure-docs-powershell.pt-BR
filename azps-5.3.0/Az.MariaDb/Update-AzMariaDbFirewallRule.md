---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7d474000ed8c449c95ae7319a960c5f748d80e66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429163"
---
# <span data-ttu-id="d1ee0-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d1ee0-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="d1ee0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ee0-103">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d1ee0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1ee0-104">SYNTAX</span></span>

### <span data-ttu-id="d1ee0-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="d1ee0-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1ee0-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d1ee0-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1ee0-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d1ee0-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1ee0-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d1ee0-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d1ee0-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1ee0-109">DESCRIPTION</span></span>
<span data-ttu-id="d1ee0-110">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d1ee0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1ee0-111">EXAMPLES</span></span>

### <span data-ttu-id="d1ee0-112">Exemplo 1: atualizar a regra de firewall MariaDB</span><span class="sxs-lookup"><span data-stu-id="d1ee0-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="d1ee0-113">Esse comando atualiza uma regra de firewall MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="d1ee0-114">Exemplo 2: atualizar a regra de firewall MariaDB por identidade.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="d1ee0-115">O cmdlet atualiza MariaDB regra de firewall por identidade.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="d1ee0-116">Exemplo 3: atualizar MariaDB regra de firewall por-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="d1ee0-117">O cmdlet atualiza MariaDB regra de firewall por-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="d1ee0-118">OS</span><span class="sxs-lookup"><span data-stu-id="d1ee0-118">PARAMETERS</span></span>

### <span data-ttu-id="d1ee0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1ee0-119">-AsJob</span></span>
<span data-ttu-id="d1ee0-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="d1ee0-120">Run the command as a job</span></span>

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

### <span data-ttu-id="d1ee0-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d1ee0-121">-ClientIPAddress</span></span>
<span data-ttu-id="d1ee0-122">Único IP especificado pelo cliente da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="d1ee0-123">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d1ee0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ee0-124">-DefaultProfile</span></span>
<span data-ttu-id="d1ee0-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1ee0-126">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="d1ee0-126">-EndIPAddress</span></span>
<span data-ttu-id="d1ee0-127">O endereço IP final da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="d1ee0-128">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d1ee0-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1ee0-129">-InputObject</span></span>
<span data-ttu-id="d1ee0-130">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ee0-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1ee0-131">-Name</span></span>
<span data-ttu-id="d1ee0-132">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="d1ee0-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d1ee0-133">-NoWait</span></span>
<span data-ttu-id="d1ee0-134">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="d1ee0-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d1ee0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1ee0-135">-ResourceGroupName</span></span>
<span data-ttu-id="d1ee0-136">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d1ee0-137">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d1ee0-138">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d1ee0-138">-ServerName</span></span>
<span data-ttu-id="d1ee0-139">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-139">The name of the server.</span></span>

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

### <span data-ttu-id="d1ee0-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="d1ee0-140">-StartIPAddress</span></span>
<span data-ttu-id="d1ee0-141">O endereço IP inicial da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="d1ee0-142">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d1ee0-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1ee0-143">-SubscriptionId</span></span>
<span data-ttu-id="d1ee0-144">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="d1ee0-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d1ee0-145">-Confirm</span></span>
<span data-ttu-id="d1ee0-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1ee0-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1ee0-147">-WhatIf</span></span>
<span data-ttu-id="d1ee0-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1ee0-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1ee0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ee0-150">CommonParameters</span></span>
<span data-ttu-id="d1ee0-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ee0-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1ee0-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ee0-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1ee0-153">INPUTS</span></span>

### <span data-ttu-id="d1ee0-154">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="d1ee0-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="d1ee0-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1ee0-155">OUTPUTS</span></span>

### <span data-ttu-id="d1ee0-156">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d1ee0-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="d1ee0-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1ee0-157">NOTES</span></span>

<span data-ttu-id="d1ee0-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d1ee0-158">ALIASES</span></span>

<span data-ttu-id="d1ee0-159">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="d1ee0-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d1ee0-160">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1ee0-161">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d1ee0-162">INPUTobject <IMariaDbIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="d1ee0-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d1ee0-163">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d1ee0-164">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d1ee0-165">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d1ee0-166">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d1ee0-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1ee0-167">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d1ee0-168">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d1ee0-169">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d1ee0-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d1ee0-171">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d1ee0-172">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="d1ee0-173">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d1ee0-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d1ee0-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1ee0-174">RELATED LINKS</span></span>

