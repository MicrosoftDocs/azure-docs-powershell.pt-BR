---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: 89c11be18fbb603f2b05fa9768a3ce05d51ddd86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888215"
---
# <span data-ttu-id="f7614-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f7614-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="f7614-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7614-102">SYNOPSIS</span></span>
<span data-ttu-id="f7614-103">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="f7614-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="f7614-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f7614-104">SYNTAX</span></span>

### <span data-ttu-id="f7614-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f7614-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f7614-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f7614-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f7614-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f7614-107">DESCRIPTION</span></span>
<span data-ttu-id="f7614-108">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="f7614-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="f7614-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7614-109">EXAMPLES</span></span>

### <span data-ttu-id="f7614-110">Exemplo 1: Atualizar a Regra de Rede Virtual PostgreSql pelo nome</span><span class="sxs-lookup"><span data-stu-id="f7614-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="f7614-111">Este cmdlet atualiza a Regra de Rede Virtual PostgreSql pelo nome.</span><span class="sxs-lookup"><span data-stu-id="f7614-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="f7614-112">Exemplo 2: Atualizar a Regra de Rede Virtual PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="f7614-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="f7614-113">Esses cmdlets atualizam a Regra de Rede Virtual PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="f7614-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="f7614-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f7614-114">PARAMETERS</span></span>

### <span data-ttu-id="f7614-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7614-115">-AsJob</span></span>
<span data-ttu-id="f7614-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="f7614-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f7614-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7614-117">-DefaultProfile</span></span>
<span data-ttu-id="f7614-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7614-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7614-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7614-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="f7614-120">Criar regra de firewall antes que a rede virtual tenha o ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="f7614-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="f7614-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7614-121">-InputObject</span></span>
<span data-ttu-id="f7614-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f7614-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7614-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f7614-123">-Name</span></span>
<span data-ttu-id="f7614-124">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f7614-124">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7614-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f7614-125">-NoWait</span></span>
<span data-ttu-id="f7614-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="f7614-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f7614-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7614-127">-PassThru</span></span>
<span data-ttu-id="f7614-128">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="f7614-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f7614-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7614-129">-ResourceGroupName</span></span>
<span data-ttu-id="f7614-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f7614-130">The name of the resource group.</span></span>
<span data-ttu-id="f7614-131">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f7614-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7614-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f7614-132">-ServerName</span></span>
<span data-ttu-id="f7614-133">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="f7614-133">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7614-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f7614-134">-SubnetId</span></span>
<span data-ttu-id="f7614-135">A ARM de recurso da sub-rede de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f7614-135">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7614-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7614-136">-SubscriptionId</span></span>
<span data-ttu-id="f7614-137">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f7614-137">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7614-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7614-138">-Confirm</span></span>
<span data-ttu-id="f7614-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7614-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7614-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7614-140">-WhatIf</span></span>
<span data-ttu-id="f7614-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f7614-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7614-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7614-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7614-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7614-143">CommonParameters</span></span>
<span data-ttu-id="f7614-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7614-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7614-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7614-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7614-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7614-146">INPUTS</span></span>

### <span data-ttu-id="f7614-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f7614-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="f7614-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f7614-148">OUTPUTS</span></span>

### <span data-ttu-id="f7614-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f7614-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="f7614-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="f7614-150">NOTES</span></span>

<span data-ttu-id="f7614-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f7614-151">ALIASES</span></span>

<span data-ttu-id="f7614-152">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="f7614-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f7614-153">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="f7614-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f7614-154">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f7614-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f7614-155">INPUTOBJECT <IPostgreSqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="f7614-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f7614-156">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="f7614-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f7614-157">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f7614-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f7614-158">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="f7614-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f7614-159">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f7614-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f7614-160">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="f7614-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f7614-161">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f7614-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f7614-162">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f7614-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="f7614-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="f7614-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f7614-164">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="f7614-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f7614-165">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f7614-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f7614-166">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f7614-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f7614-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7614-167">RELATED LINKS</span></span>

