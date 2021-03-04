---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: cbb774e0a4bedb66a32839c069c305317c8e9f43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892134"
---
# <span data-ttu-id="ead22-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ead22-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="ead22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ead22-102">SYNOPSIS</span></span>
<span data-ttu-id="ead22-103">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="ead22-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="ead22-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ead22-104">SYNTAX</span></span>

### <span data-ttu-id="ead22-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ead22-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ead22-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ead22-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ead22-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ead22-107">DESCRIPTION</span></span>
<span data-ttu-id="ead22-108">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="ead22-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="ead22-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ead22-109">EXAMPLES</span></span>

### <span data-ttu-id="ead22-110">Exemplo 1: Atualizar a regra de rede virtual do MariaDB</span><span class="sxs-lookup"><span data-stu-id="ead22-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="ead22-111">Este comando atualiza uma regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ead22-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="ead22-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ead22-112">PARAMETERS</span></span>

### <span data-ttu-id="ead22-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ead22-113">-AsJob</span></span>
<span data-ttu-id="ead22-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ead22-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ead22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead22-115">-DefaultProfile</span></span>
<span data-ttu-id="ead22-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ead22-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ead22-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ead22-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="ead22-118">Criar regra de firewall antes que a rede virtual tenha o ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="ead22-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="ead22-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ead22-119">-InputObject</span></span>
<span data-ttu-id="ead22-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ead22-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ead22-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ead22-121">-Name</span></span>
<span data-ttu-id="ead22-122">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ead22-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="ead22-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ead22-123">-NoWait</span></span>
<span data-ttu-id="ead22-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="ead22-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ead22-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ead22-125">-PassThru</span></span>
<span data-ttu-id="ead22-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="ead22-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ead22-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ead22-127">-ResourceGroupName</span></span>
<span data-ttu-id="ead22-128">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="ead22-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ead22-129">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="ead22-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ead22-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ead22-130">-ServerName</span></span>
<span data-ttu-id="ead22-131">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="ead22-131">The name of the server.</span></span>

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

### <span data-ttu-id="ead22-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ead22-132">-SubnetId</span></span>
<span data-ttu-id="ead22-133">A ARM de recurso da sub-rede de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ead22-133">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead22-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ead22-134">-SubscriptionId</span></span>
<span data-ttu-id="ead22-135">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ead22-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ead22-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ead22-136">-Confirm</span></span>
<span data-ttu-id="ead22-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ead22-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ead22-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead22-138">-WhatIf</span></span>
<span data-ttu-id="ead22-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ead22-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ead22-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ead22-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ead22-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead22-141">CommonParameters</span></span>
<span data-ttu-id="ead22-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ead22-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead22-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ead22-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead22-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ead22-144">INPUTS</span></span>

### <span data-ttu-id="ead22-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="ead22-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="ead22-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ead22-146">OUTPUTS</span></span>

### <span data-ttu-id="ead22-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ead22-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="ead22-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="ead22-148">NOTES</span></span>

<span data-ttu-id="ead22-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ead22-149">ALIASES</span></span>

<span data-ttu-id="ead22-150">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="ead22-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ead22-151">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ead22-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ead22-152">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ead22-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ead22-153">INPUTOBJECT <IMariaDbIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="ead22-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ead22-154">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="ead22-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ead22-155">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ead22-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ead22-156">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="ead22-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ead22-157">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ead22-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ead22-158">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="ead22-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ead22-159">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="ead22-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ead22-160">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="ead22-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ead22-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="ead22-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ead22-162">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="ead22-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ead22-163">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ead22-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="ead22-164">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ead22-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ead22-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ead22-165">RELATED LINKS</span></span>

