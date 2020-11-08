---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: c4eb244dd2d1a0d685bf18f39deedf9992b5597e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118399"
---
# <span data-ttu-id="e4458-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4458-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="e4458-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4458-102">SYNOPSIS</span></span>
<span data-ttu-id="e4458-103">Atualiza uma configuração de um servidor.</span><span class="sxs-lookup"><span data-stu-id="e4458-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="e4458-104">Use Update-AzMySqlServer em vez disso, se quiser atualizar AdministratorLoginPassword, SKU, etc.</span><span class="sxs-lookup"><span data-stu-id="e4458-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="e4458-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4458-105">SYNTAX</span></span>

### <span data-ttu-id="e4458-106">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="e4458-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e4458-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e4458-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e4458-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4458-108">DESCRIPTION</span></span>
<span data-ttu-id="e4458-109">Atualiza uma configuração de um servidor.</span><span class="sxs-lookup"><span data-stu-id="e4458-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="e4458-110">Use Update-AzMySqlServer em vez disso, se quiser atualizar AdministratorLoginPassword, SKU, etc.</span><span class="sxs-lookup"><span data-stu-id="e4458-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="e4458-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4458-111">EXAMPLES</span></span>

### <span data-ttu-id="e4458-112">Exemplo 1: atualizar a configuração do MySql por nome</span><span class="sxs-lookup"><span data-stu-id="e4458-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="e4458-113">Este cmdlet atualiza a configuração de MySql por nome.</span><span class="sxs-lookup"><span data-stu-id="e4458-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="e4458-114">Exemplo 2: Atualize a configuração do MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="e4458-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="e4458-115">Esses cmdlets atualizam a configuração do MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="e4458-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="e4458-116">OS</span><span class="sxs-lookup"><span data-stu-id="e4458-116">PARAMETERS</span></span>

### <span data-ttu-id="e4458-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4458-117">-AsJob</span></span>
<span data-ttu-id="e4458-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="e4458-118">Run the command as a job</span></span>

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

### <span data-ttu-id="e4458-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4458-119">-DefaultProfile</span></span>
<span data-ttu-id="e4458-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4458-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4458-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4458-121">-InputObject</span></span>
<span data-ttu-id="e4458-122">Parâmetro de identidade.</span><span class="sxs-lookup"><span data-stu-id="e4458-122">Identity Parameter.</span></span>
<span data-ttu-id="e4458-123">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e4458-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4458-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4458-124">-Name</span></span>
<span data-ttu-id="e4458-125">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="e4458-125">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4458-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e4458-126">-NoWait</span></span>
<span data-ttu-id="e4458-127">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="e4458-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e4458-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4458-128">-ResourceGroupName</span></span>
<span data-ttu-id="e4458-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4458-129">The name of the resource group.</span></span>
<span data-ttu-id="e4458-130">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e4458-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e4458-131">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e4458-131">-ServerName</span></span>
<span data-ttu-id="e4458-132">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="e4458-132">The name of the server.</span></span>

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

### <span data-ttu-id="e4458-133">-Fonte</span><span class="sxs-lookup"><span data-stu-id="e4458-133">-Source</span></span>
<span data-ttu-id="e4458-134">Fonte da configuração.</span><span class="sxs-lookup"><span data-stu-id="e4458-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="e4458-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4458-135">-SubscriptionId</span></span>
<span data-ttu-id="e4458-136">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="e4458-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e4458-137">-Valor</span><span class="sxs-lookup"><span data-stu-id="e4458-137">-Value</span></span>
<span data-ttu-id="e4458-138">Valor da configuração.</span><span class="sxs-lookup"><span data-stu-id="e4458-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="e4458-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4458-139">-Confirm</span></span>
<span data-ttu-id="e4458-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4458-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4458-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4458-141">-WhatIf</span></span>
<span data-ttu-id="e4458-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4458-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4458-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4458-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4458-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4458-144">CommonParameters</span></span>
<span data-ttu-id="e4458-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4458-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4458-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4458-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4458-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4458-147">INPUTS</span></span>

### <span data-ttu-id="e4458-148">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e4458-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="e4458-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4458-149">OUTPUTS</span></span>

### <span data-ttu-id="e4458-150">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4458-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="e4458-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4458-151">NOTES</span></span>

<span data-ttu-id="e4458-152">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e4458-152">ALIASES</span></span>

<span data-ttu-id="e4458-153">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="e4458-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e4458-154">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="e4458-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4458-155">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e4458-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e4458-156">INPUTobject <IMySqlIdentity> : Parameter de identidade.</span><span class="sxs-lookup"><span data-stu-id="e4458-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="e4458-157">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="e4458-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e4458-158">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e4458-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e4458-159">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="e4458-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e4458-160">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e4458-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e4458-161">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="e4458-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e4458-162">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4458-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e4458-163">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e4458-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="e4458-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="e4458-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e4458-165">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="e4458-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e4458-166">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="e4458-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e4458-167">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e4458-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e4458-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4458-168">RELATED LINKS</span></span>

