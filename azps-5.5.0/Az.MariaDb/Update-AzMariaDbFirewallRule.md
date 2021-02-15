---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7d474000ed8c449c95ae7319a960c5f748d80e66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111786"
---
# <span data-ttu-id="6b060-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6b060-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="6b060-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b060-102">SYNOPSIS</span></span>
<span data-ttu-id="6b060-103">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="6b060-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="6b060-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b060-104">SYNTAX</span></span>

### <span data-ttu-id="6b060-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6b060-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b060-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="6b060-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b060-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6b060-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b060-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6b060-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6b060-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b060-109">DESCRIPTION</span></span>
<span data-ttu-id="6b060-110">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="6b060-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="6b060-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6b060-111">EXAMPLES</span></span>

### <span data-ttu-id="6b060-112">Exemplo 1: Atualizar regra de firewall mariadb</span><span class="sxs-lookup"><span data-stu-id="6b060-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="6b060-113">Este comando atualiza uma regra de firewall MariaDB.</span><span class="sxs-lookup"><span data-stu-id="6b060-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="6b060-114">Exemplo 2: Atualizar a Regra de Firewall mariadb por identidade.</span><span class="sxs-lookup"><span data-stu-id="6b060-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="6b060-115">O cmdlet atualiza a Regra de Firewall mariadb por identidade.</span><span class="sxs-lookup"><span data-stu-id="6b060-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="6b060-116">Exemplo 3: Atualizar a Regra de Firewall mariadb por -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="6b060-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="6b060-117">O cmdlet atualiza a Regra de Firewall de MariaDB por -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="6b060-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="6b060-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b060-118">PARAMETERS</span></span>

### <span data-ttu-id="6b060-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b060-119">-AsJob</span></span>
<span data-ttu-id="6b060-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="6b060-120">Run the command as a job</span></span>

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

### <span data-ttu-id="6b060-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="6b060-121">-ClientIPAddress</span></span>
<span data-ttu-id="6b060-122">O cliente especificou um ÚNICO IP da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="6b060-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="6b060-123">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="6b060-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6b060-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b060-124">-DefaultProfile</span></span>
<span data-ttu-id="6b060-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b060-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b060-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="6b060-126">-EndIPAddress</span></span>
<span data-ttu-id="6b060-127">O endereço IP final da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="6b060-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="6b060-128">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="6b060-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6b060-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b060-129">-InputObject</span></span>
<span data-ttu-id="6b060-130">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="6b060-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6b060-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b060-131">-Name</span></span>
<span data-ttu-id="6b060-132">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="6b060-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="6b060-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6b060-133">-NoWait</span></span>
<span data-ttu-id="6b060-134">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="6b060-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6b060-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b060-135">-ResourceGroupName</span></span>
<span data-ttu-id="6b060-136">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="6b060-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6b060-137">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="6b060-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6b060-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6b060-138">-ServerName</span></span>
<span data-ttu-id="6b060-139">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="6b060-139">The name of the server.</span></span>

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

### <span data-ttu-id="6b060-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="6b060-140">-StartIPAddress</span></span>
<span data-ttu-id="6b060-141">O endereço IP inicial da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="6b060-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="6b060-142">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="6b060-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6b060-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b060-143">-SubscriptionId</span></span>
<span data-ttu-id="6b060-144">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b060-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6b060-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6b060-145">-Confirm</span></span>
<span data-ttu-id="6b060-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b060-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b060-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b060-147">-WhatIf</span></span>
<span data-ttu-id="6b060-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6b060-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b060-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b060-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b060-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b060-150">CommonParameters</span></span>
<span data-ttu-id="6b060-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b060-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b060-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b060-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b060-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="6b060-153">INPUTS</span></span>

### <span data-ttu-id="6b060-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="6b060-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="6b060-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="6b060-155">OUTPUTS</span></span>

### <span data-ttu-id="6b060-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6b060-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="6b060-157">Notas</span><span class="sxs-lookup"><span data-stu-id="6b060-157">NOTES</span></span>

<span data-ttu-id="6b060-158">Aliases</span><span class="sxs-lookup"><span data-stu-id="6b060-158">ALIASES</span></span>

<span data-ttu-id="6b060-159">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="6b060-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b060-160">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="6b060-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b060-161">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b060-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b060-162">INPUTOBJECT: <IMariaDbIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="6b060-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b060-163">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="6b060-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6b060-164">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6b060-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6b060-165">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="6b060-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6b060-166">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="6b060-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b060-167">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="6b060-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6b060-168">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="6b060-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6b060-169">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="6b060-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6b060-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="6b060-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6b060-171">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="6b060-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6b060-172">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b060-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="6b060-173">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6b060-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6b060-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b060-174">RELATED LINKS</span></span>

