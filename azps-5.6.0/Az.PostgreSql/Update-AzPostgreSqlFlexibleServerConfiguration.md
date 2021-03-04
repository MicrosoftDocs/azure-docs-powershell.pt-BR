---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: e45d342f7bb02034b2adf0473e6d4d1eb3c2b370
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888218"
---
# <span data-ttu-id="263b0-101">Update-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="263b0-101">Update-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="263b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="263b0-102">SYNOPSIS</span></span>
<span data-ttu-id="263b0-103">Atualiza uma configuração de um servidor.</span><span class="sxs-lookup"><span data-stu-id="263b0-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="263b0-104">Use Update-AzPostgreSqlFlexibleServer em vez disso, se quiser atualizar AdministratorLoginPassword, sku, etc.</span><span class="sxs-lookup"><span data-stu-id="263b0-104">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="263b0-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="263b0-105">SYNTAX</span></span>

### <span data-ttu-id="263b0-106">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="263b0-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="263b0-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="263b0-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>]
 [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="263b0-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="263b0-108">DESCRIPTION</span></span>
<span data-ttu-id="263b0-109">Atualiza uma configuração de um servidor.</span><span class="sxs-lookup"><span data-stu-id="263b0-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="263b0-110">Use Update-AzPostgreSqlFlexibleServer em vez disso, se quiser atualizar AdministratorLoginPassword, sku, etc.</span><span class="sxs-lookup"><span data-stu-id="263b0-110">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="263b0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="263b0-111">EXAMPLES</span></span>

### <span data-ttu-id="263b0-112">Exemplo 1: Configuração de PostgreSql especificada por nome</span><span class="sxs-lookup"><span data-stu-id="263b0-112">Example 1: Updatae specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="263b0-113">Este cmdlet atualiza a configuração de PostgreSql especificada pelo nome.</span><span class="sxs-lookup"><span data-stu-id="263b0-113">This cmdlet updates specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="263b0-114">Exemplo 1: Configuração de PostgreSql especificada por identidade</span><span class="sxs-lookup"><span data-stu-id="263b0-114">Example 1: Updatae specified PostgreSql configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/configurations/work_mem"
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default  4096-2097151   Integer
```

<span data-ttu-id="263b0-115">Este cmdlet atualiza a configuração de PostgreSql especificada por identidade.</span><span class="sxs-lookup"><span data-stu-id="263b0-115">This cmdlet updates specified PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="263b0-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="263b0-116">PARAMETERS</span></span>

### <span data-ttu-id="263b0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="263b0-117">-AsJob</span></span>
<span data-ttu-id="263b0-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="263b0-118">Run the command as a job</span></span>

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

### <span data-ttu-id="263b0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="263b0-119">-DefaultProfile</span></span>
<span data-ttu-id="263b0-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="263b0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="263b0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="263b0-121">-InputObject</span></span>
<span data-ttu-id="263b0-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="263b0-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="263b0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="263b0-123">-Name</span></span>
<span data-ttu-id="263b0-124">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="263b0-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="263b0-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="263b0-125">-NoWait</span></span>
<span data-ttu-id="263b0-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="263b0-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="263b0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="263b0-127">-ResourceGroupName</span></span>
<span data-ttu-id="263b0-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="263b0-128">The name of the resource group.</span></span>
<span data-ttu-id="263b0-129">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="263b0-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="263b0-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="263b0-130">-ServerName</span></span>
<span data-ttu-id="263b0-131">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="263b0-131">The name of the server.</span></span>

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

### <span data-ttu-id="263b0-132">-Source</span><span class="sxs-lookup"><span data-stu-id="263b0-132">-Source</span></span>
<span data-ttu-id="263b0-133">Origem da configuração.</span><span class="sxs-lookup"><span data-stu-id="263b0-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="263b0-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="263b0-134">-SubscriptionId</span></span>
<span data-ttu-id="263b0-135">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="263b0-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="263b0-136">-Value</span><span class="sxs-lookup"><span data-stu-id="263b0-136">-Value</span></span>
<span data-ttu-id="263b0-137">Valor da configuração.</span><span class="sxs-lookup"><span data-stu-id="263b0-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="263b0-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="263b0-138">-Confirm</span></span>
<span data-ttu-id="263b0-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="263b0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="263b0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="263b0-140">-WhatIf</span></span>
<span data-ttu-id="263b0-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="263b0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="263b0-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="263b0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="263b0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="263b0-143">CommonParameters</span></span>
<span data-ttu-id="263b0-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="263b0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="263b0-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="263b0-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="263b0-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="263b0-146">INPUTS</span></span>

### <span data-ttu-id="263b0-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="263b0-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="263b0-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="263b0-148">OUTPUTS</span></span>

### <span data-ttu-id="263b0-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="263b0-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="263b0-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="263b0-150">NOTES</span></span>

<span data-ttu-id="263b0-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="263b0-151">ALIASES</span></span>

<span data-ttu-id="263b0-152">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="263b0-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="263b0-153">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="263b0-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="263b0-154">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="263b0-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="263b0-155">INPUTOBJECT <IPostgreSqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="263b0-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="263b0-156">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="263b0-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="263b0-157">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="263b0-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="263b0-158">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="263b0-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="263b0-159">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="263b0-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="263b0-160">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="263b0-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="263b0-161">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="263b0-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="263b0-162">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="263b0-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="263b0-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="263b0-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="263b0-164">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="263b0-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="263b0-165">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="263b0-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="263b0-166">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="263b0-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="263b0-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="263b0-167">RELATED LINKS</span></span>

