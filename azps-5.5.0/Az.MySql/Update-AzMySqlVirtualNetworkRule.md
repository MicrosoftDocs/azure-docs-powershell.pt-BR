---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 7779a5405f50fe87f7a9e631b40cbdc8cb40fe5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111723"
---
# <span data-ttu-id="470c8-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="470c8-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="470c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="470c8-102">SYNOPSIS</span></span>
<span data-ttu-id="470c8-103">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="470c8-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="470c8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="470c8-104">SYNTAX</span></span>

### <span data-ttu-id="470c8-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="470c8-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="470c8-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="470c8-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="470c8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="470c8-107">DESCRIPTION</span></span>
<span data-ttu-id="470c8-108">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="470c8-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="470c8-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="470c8-109">EXAMPLES</span></span>

### <span data-ttu-id="470c8-110">Exemplo 1: Atualizar MySql Virtual Network Rule por nome</span><span class="sxs-lookup"><span data-stu-id="470c8-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="470c8-111">Este cmdlet atualiza a MySql Virtual Network Rule por nome.</span><span class="sxs-lookup"><span data-stu-id="470c8-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="470c8-112">Exemplo 2: Atualizar a Regra de Rede Virtual MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="470c8-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="470c8-113">Esses cmdlets atualizam a Regra de Rede Virtual MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="470c8-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="470c8-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="470c8-114">PARAMETERS</span></span>

### <span data-ttu-id="470c8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="470c8-115">-AsJob</span></span>
<span data-ttu-id="470c8-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="470c8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="470c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="470c8-117">-DefaultProfile</span></span>
<span data-ttu-id="470c8-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="470c8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="470c8-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="470c8-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="470c8-120">Crie uma regra de firewall antes que a rede virtual tenha o ponto de extremidade do serviço VNET habilitado.</span><span class="sxs-lookup"><span data-stu-id="470c8-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="470c8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="470c8-121">-InputObject</span></span>
<span data-ttu-id="470c8-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="470c8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="470c8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="470c8-123">-Name</span></span>
<span data-ttu-id="470c8-124">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="470c8-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="470c8-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="470c8-125">-NoWait</span></span>
<span data-ttu-id="470c8-126">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="470c8-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="470c8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="470c8-127">-PassThru</span></span>
<span data-ttu-id="470c8-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="470c8-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="470c8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="470c8-129">-ResourceGroupName</span></span>
<span data-ttu-id="470c8-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="470c8-130">The name of the resource group.</span></span>
<span data-ttu-id="470c8-131">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="470c8-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="470c8-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="470c8-132">-ServerName</span></span>
<span data-ttu-id="470c8-133">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="470c8-133">The name of the server.</span></span>

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

### <span data-ttu-id="470c8-134">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="470c8-134">-SubnetId</span></span>
<span data-ttu-id="470c8-135">A ID do recurso ARM da sub-rede virtual.</span><span class="sxs-lookup"><span data-stu-id="470c8-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="470c8-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="470c8-136">-SubscriptionId</span></span>
<span data-ttu-id="470c8-137">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="470c8-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="470c8-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="470c8-138">-Confirm</span></span>
<span data-ttu-id="470c8-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="470c8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="470c8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="470c8-140">-WhatIf</span></span>
<span data-ttu-id="470c8-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="470c8-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="470c8-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="470c8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="470c8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="470c8-143">CommonParameters</span></span>
<span data-ttu-id="470c8-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="470c8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="470c8-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="470c8-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="470c8-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="470c8-146">INPUTS</span></span>

### <span data-ttu-id="470c8-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="470c8-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="470c8-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="470c8-148">OUTPUTS</span></span>

### <span data-ttu-id="470c8-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="470c8-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="470c8-150">Notas</span><span class="sxs-lookup"><span data-stu-id="470c8-150">NOTES</span></span>

<span data-ttu-id="470c8-151">Aliases</span><span class="sxs-lookup"><span data-stu-id="470c8-151">ALIASES</span></span>

<span data-ttu-id="470c8-152">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="470c8-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="470c8-153">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="470c8-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="470c8-154">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="470c8-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="470c8-155">INPUTOBJECT: <IMySqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="470c8-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="470c8-156">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="470c8-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="470c8-157">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="470c8-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="470c8-158">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="470c8-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="470c8-159">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="470c8-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="470c8-160">`[KeyName <String>]`: o nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="470c8-160">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="470c8-161">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="470c8-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="470c8-162">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="470c8-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="470c8-163">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="470c8-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="470c8-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="470c8-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="470c8-165">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="470c8-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="470c8-166">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="470c8-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="470c8-167">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="470c8-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="470c8-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="470c8-168">RELATED LINKS</span></span>

