---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: f98c24ab0be3b2c35ac43642fb9d4bbf0b421c7e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111620"
---
# <span data-ttu-id="0ae92-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0ae92-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="0ae92-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ae92-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae92-103">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="0ae92-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="0ae92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ae92-104">SYNTAX</span></span>

### <span data-ttu-id="0ae92-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="0ae92-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0ae92-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0ae92-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0ae92-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0ae92-107">DESCRIPTION</span></span>
<span data-ttu-id="0ae92-108">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="0ae92-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="0ae92-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0ae92-109">EXAMPLES</span></span>

### <span data-ttu-id="0ae92-110">Exemplo 1: atualizar a regra de rede virtual do MySql por nome</span><span class="sxs-lookup"><span data-stu-id="0ae92-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="0ae92-111">Este cmdlet atualiza a regra de rede virtual do MySql por nome.</span><span class="sxs-lookup"><span data-stu-id="0ae92-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="0ae92-112">Exemplo 2: atualizar a regra de rede virtual do MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="0ae92-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="0ae92-113">Esses cmdlets atualizam a regra de rede virtual do MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="0ae92-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="0ae92-114">OS</span><span class="sxs-lookup"><span data-stu-id="0ae92-114">PARAMETERS</span></span>

### <span data-ttu-id="0ae92-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ae92-115">-AsJob</span></span>
<span data-ttu-id="0ae92-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="0ae92-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0ae92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ae92-117">-DefaultProfile</span></span>
<span data-ttu-id="0ae92-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0ae92-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ae92-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="0ae92-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="0ae92-120">Crie uma regra de firewall antes da rede virtual ter ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="0ae92-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="0ae92-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ae92-121">-InputObject</span></span>
<span data-ttu-id="0ae92-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0ae92-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ae92-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ae92-123">-Name</span></span>
<span data-ttu-id="0ae92-124">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0ae92-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="0ae92-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0ae92-125">-NoWait</span></span>
<span data-ttu-id="0ae92-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="0ae92-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0ae92-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ae92-127">-PassThru</span></span>
<span data-ttu-id="0ae92-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="0ae92-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0ae92-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ae92-129">-ResourceGroupName</span></span>
<span data-ttu-id="0ae92-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0ae92-130">The name of the resource group.</span></span>
<span data-ttu-id="0ae92-131">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0ae92-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0ae92-132">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="0ae92-132">-ServerName</span></span>
<span data-ttu-id="0ae92-133">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="0ae92-133">The name of the server.</span></span>

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

### <span data-ttu-id="0ae92-134">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="0ae92-134">-SubnetId</span></span>
<span data-ttu-id="0ae92-135">A ID do recurso ARM da sub-rede da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0ae92-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="0ae92-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ae92-136">-SubscriptionId</span></span>
<span data-ttu-id="0ae92-137">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="0ae92-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0ae92-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0ae92-138">-Confirm</span></span>
<span data-ttu-id="0ae92-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ae92-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ae92-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ae92-140">-WhatIf</span></span>
<span data-ttu-id="0ae92-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0ae92-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ae92-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0ae92-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ae92-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ae92-143">CommonParameters</span></span>
<span data-ttu-id="0ae92-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ae92-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ae92-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ae92-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ae92-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0ae92-146">INPUTS</span></span>

### <span data-ttu-id="0ae92-147">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0ae92-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="0ae92-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0ae92-148">OUTPUTS</span></span>

### <span data-ttu-id="0ae92-149">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0ae92-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="0ae92-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0ae92-150">NOTES</span></span>

<span data-ttu-id="0ae92-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0ae92-151">ALIASES</span></span>

<span data-ttu-id="0ae92-152">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="0ae92-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0ae92-153">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="0ae92-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ae92-154">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0ae92-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0ae92-155">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="0ae92-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0ae92-156">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="0ae92-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0ae92-157">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0ae92-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0ae92-158">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="0ae92-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0ae92-159">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="0ae92-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0ae92-160">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="0ae92-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0ae92-161">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0ae92-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0ae92-162">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0ae92-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="0ae92-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="0ae92-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0ae92-164">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="0ae92-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0ae92-165">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="0ae92-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0ae92-166">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0ae92-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0ae92-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ae92-167">RELATED LINKS</span></span>

