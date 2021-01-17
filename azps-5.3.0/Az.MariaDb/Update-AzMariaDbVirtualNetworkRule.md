---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 9ec9113ba17ec28e7cef934a4b857e4cbf0acce0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429161"
---
# <span data-ttu-id="5cb25-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5cb25-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="5cb25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5cb25-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb25-103">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="5cb25-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="5cb25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5cb25-104">SYNTAX</span></span>

### <span data-ttu-id="5cb25-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="5cb25-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5cb25-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5cb25-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5cb25-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5cb25-107">DESCRIPTION</span></span>
<span data-ttu-id="5cb25-108">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="5cb25-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="5cb25-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5cb25-109">EXAMPLES</span></span>

### <span data-ttu-id="5cb25-110">Exemplo 1: atualizar a regra de rede virtual MariaDB</span><span class="sxs-lookup"><span data-stu-id="5cb25-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="5cb25-111">Este comando atualiza uma regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5cb25-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="5cb25-112">OS</span><span class="sxs-lookup"><span data-stu-id="5cb25-112">PARAMETERS</span></span>

### <span data-ttu-id="5cb25-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cb25-113">-AsJob</span></span>
<span data-ttu-id="5cb25-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="5cb25-114">Run the command as a job</span></span>

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

### <span data-ttu-id="5cb25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb25-115">-DefaultProfile</span></span>
<span data-ttu-id="5cb25-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb25-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cb25-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5cb25-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="5cb25-118">Crie uma regra de firewall antes da rede virtual ter ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="5cb25-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="5cb25-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cb25-119">-InputObject</span></span>
<span data-ttu-id="5cb25-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5cb25-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5cb25-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5cb25-121">-Name</span></span>
<span data-ttu-id="5cb25-122">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5cb25-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="5cb25-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5cb25-123">-NoWait</span></span>
<span data-ttu-id="5cb25-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="5cb25-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5cb25-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cb25-125">-PassThru</span></span>
<span data-ttu-id="5cb25-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="5cb25-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5cb25-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb25-127">-ResourceGroupName</span></span>
<span data-ttu-id="5cb25-128">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="5cb25-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5cb25-129">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="5cb25-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5cb25-130">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="5cb25-130">-ServerName</span></span>
<span data-ttu-id="5cb25-131">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="5cb25-131">The name of the server.</span></span>

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

### <span data-ttu-id="5cb25-132">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="5cb25-132">-SubnetId</span></span>
<span data-ttu-id="5cb25-133">A ID do recurso ARM da sub-rede da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5cb25-133">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="5cb25-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cb25-134">-SubscriptionId</span></span>
<span data-ttu-id="5cb25-135">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb25-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="5cb25-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5cb25-136">-Confirm</span></span>
<span data-ttu-id="5cb25-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cb25-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cb25-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cb25-138">-WhatIf</span></span>
<span data-ttu-id="5cb25-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5cb25-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cb25-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5cb25-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cb25-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb25-141">CommonParameters</span></span>
<span data-ttu-id="5cb25-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cb25-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb25-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cb25-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb25-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5cb25-144">INPUTS</span></span>

### <span data-ttu-id="5cb25-145">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="5cb25-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="5cb25-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5cb25-146">OUTPUTS</span></span>

### <span data-ttu-id="5cb25-147">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5cb25-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="5cb25-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5cb25-148">NOTES</span></span>

<span data-ttu-id="5cb25-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5cb25-149">ALIASES</span></span>

<span data-ttu-id="5cb25-150">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="5cb25-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5cb25-151">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="5cb25-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5cb25-152">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5cb25-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5cb25-153">INPUTobject <IMariaDbIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="5cb25-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5cb25-154">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="5cb25-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5cb25-155">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5cb25-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5cb25-156">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="5cb25-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5cb25-157">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="5cb25-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5cb25-158">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="5cb25-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5cb25-159">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="5cb25-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="5cb25-160">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="5cb25-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="5cb25-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="5cb25-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5cb25-162">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="5cb25-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5cb25-163">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb25-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="5cb25-164">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5cb25-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5cb25-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5cb25-165">RELATED LINKS</span></span>

