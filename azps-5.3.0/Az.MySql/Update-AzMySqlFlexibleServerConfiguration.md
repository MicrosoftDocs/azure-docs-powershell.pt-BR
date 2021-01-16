---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 7e3c3855fb36d1dbc96b399d5348f033ca74908e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428224"
---
# <span data-ttu-id="544d2-101">Update-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="544d2-101">Update-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="544d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="544d2-102">SYNOPSIS</span></span>
<span data-ttu-id="544d2-103">Atualiza as informações sobre uma configuração de um servidor flexível do MySQL.</span><span class="sxs-lookup"><span data-stu-id="544d2-103">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="544d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="544d2-104">SYNTAX</span></span>

### <span data-ttu-id="544d2-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="544d2-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="544d2-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="544d2-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="544d2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="544d2-107">DESCRIPTION</span></span>
<span data-ttu-id="544d2-108">Atualiza as informações sobre uma configuração de um servidor flexível do MySQL.</span><span class="sxs-lookup"><span data-stu-id="544d2-108">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="544d2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="544d2-109">EXAMPLES</span></span>

### <span data-ttu-id="544d2-110">Exemplo 1: atualizar a configuração do MySql por nome</span><span class="sxs-lookup"><span data-stu-id="544d2-110">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
net_retry_count 15    10            user-override  1-4294967295   Integer
```

<span data-ttu-id="544d2-111">Este cmdlet atualiza a configuração de MySql por nome.</span><span class="sxs-lookup"><span data-stu-id="544d2-111">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="544d2-112">Exemplo 2: Atualize a configuração do MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="544d2-112">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlFlexibleServer -InputObject $ID -Value 150

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   150    28800         system-default   1-31536000   Integer
```

<span data-ttu-id="544d2-113">Esses cmdlets atualizam a configuração do MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="544d2-113">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="544d2-114">OS</span><span class="sxs-lookup"><span data-stu-id="544d2-114">PARAMETERS</span></span>

### <span data-ttu-id="544d2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="544d2-115">-AsJob</span></span>
<span data-ttu-id="544d2-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="544d2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="544d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="544d2-117">-DefaultProfile</span></span>
<span data-ttu-id="544d2-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="544d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="544d2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="544d2-119">-InputObject</span></span>
<span data-ttu-id="544d2-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="544d2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="544d2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="544d2-121">-Name</span></span>
<span data-ttu-id="544d2-122">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="544d2-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="544d2-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="544d2-123">-NoWait</span></span>
<span data-ttu-id="544d2-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="544d2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="544d2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="544d2-125">-ResourceGroupName</span></span>
<span data-ttu-id="544d2-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="544d2-126">The name of the resource group.</span></span>
<span data-ttu-id="544d2-127">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="544d2-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="544d2-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="544d2-128">-ServerName</span></span>
<span data-ttu-id="544d2-129">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="544d2-129">The name of the server.</span></span>

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

### <span data-ttu-id="544d2-130">-Fonte</span><span class="sxs-lookup"><span data-stu-id="544d2-130">-Source</span></span>
<span data-ttu-id="544d2-131">A origem do valor de atualização.</span><span class="sxs-lookup"><span data-stu-id="544d2-131">The source of the updating value.</span></span>
<span data-ttu-id="544d2-132">O valor padrão é User-override</span><span class="sxs-lookup"><span data-stu-id="544d2-132">The default value is user-override</span></span>

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

### <span data-ttu-id="544d2-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="544d2-133">-SubscriptionId</span></span>
<span data-ttu-id="544d2-134">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="544d2-134">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="544d2-135">-Valor</span><span class="sxs-lookup"><span data-stu-id="544d2-135">-Value</span></span>
<span data-ttu-id="544d2-136">Valor da configuração.</span><span class="sxs-lookup"><span data-stu-id="544d2-136">Value of the configuration.</span></span>

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

### <span data-ttu-id="544d2-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="544d2-137">-Confirm</span></span>
<span data-ttu-id="544d2-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="544d2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="544d2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="544d2-139">-WhatIf</span></span>
<span data-ttu-id="544d2-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="544d2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="544d2-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="544d2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="544d2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="544d2-142">CommonParameters</span></span>
<span data-ttu-id="544d2-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="544d2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="544d2-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="544d2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="544d2-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="544d2-145">INPUTS</span></span>

### <span data-ttu-id="544d2-146">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="544d2-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="544d2-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="544d2-147">OUTPUTS</span></span>

### <span data-ttu-id="544d2-148">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20200701Preview. IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="544d2-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="544d2-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="544d2-149">NOTES</span></span>

<span data-ttu-id="544d2-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="544d2-150">ALIASES</span></span>

<span data-ttu-id="544d2-151">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="544d2-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="544d2-152">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="544d2-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="544d2-153">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="544d2-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="544d2-154">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="544d2-154">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="544d2-155">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="544d2-155">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="544d2-156">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="544d2-156">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="544d2-157">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="544d2-157">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="544d2-158">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="544d2-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="544d2-159">`[KeyName <String>]`: O nome da tecla do servidor.</span><span class="sxs-lookup"><span data-stu-id="544d2-159">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="544d2-160">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="544d2-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="544d2-161">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="544d2-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="544d2-162">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="544d2-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="544d2-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="544d2-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="544d2-164">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="544d2-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="544d2-165">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="544d2-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="544d2-166">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="544d2-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="544d2-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="544d2-167">RELATED LINKS</span></span>

