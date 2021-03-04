---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 98e476b2a1732d2c984d200265d817c3ff6d71a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887484"
---
# <span data-ttu-id="d0c21-101">Update-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0c21-101">Update-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="d0c21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0c21-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c21-103">Atualiza informações sobre uma configuração de um servidor mySQL flexível.</span><span class="sxs-lookup"><span data-stu-id="d0c21-103">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="d0c21-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d0c21-104">SYNTAX</span></span>

### <span data-ttu-id="d0c21-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d0c21-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d0c21-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d0c21-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d0c21-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d0c21-107">DESCRIPTION</span></span>
<span data-ttu-id="d0c21-108">Atualiza informações sobre uma configuração de um servidor mySQL flexível.</span><span class="sxs-lookup"><span data-stu-id="d0c21-108">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="d0c21-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0c21-109">EXAMPLES</span></span>

### <span data-ttu-id="d0c21-110">Exemplo 1: Atualizar a configuração do MySql pelo nome</span><span class="sxs-lookup"><span data-stu-id="d0c21-110">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
net_retry_count 15    10            user-override  1-4294967295   Integer
```

<span data-ttu-id="d0c21-111">Este cmdlet atualiza a configuração do MySql pelo nome.</span><span class="sxs-lookup"><span data-stu-id="d0c21-111">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="d0c21-112">Exemplo 2: atualizar a configuração do MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="d0c21-112">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlFlexibleServer -InputObject $ID -Value 150

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   150    28800         system-default   1-31536000   Integer
```

<span data-ttu-id="d0c21-113">Esses cmdlets atualizam a configuração do MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="d0c21-113">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="d0c21-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d0c21-114">PARAMETERS</span></span>

### <span data-ttu-id="d0c21-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0c21-115">-AsJob</span></span>
<span data-ttu-id="d0c21-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="d0c21-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d0c21-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0c21-117">-DefaultProfile</span></span>
<span data-ttu-id="d0c21-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0c21-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0c21-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0c21-119">-InputObject</span></span>
<span data-ttu-id="d0c21-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d0c21-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d0c21-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d0c21-121">-Name</span></span>
<span data-ttu-id="d0c21-122">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="d0c21-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="d0c21-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d0c21-123">-NoWait</span></span>
<span data-ttu-id="d0c21-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="d0c21-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d0c21-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0c21-125">-ResourceGroupName</span></span>
<span data-ttu-id="d0c21-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d0c21-126">The name of the resource group.</span></span>
<span data-ttu-id="d0c21-127">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d0c21-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d0c21-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d0c21-128">-ServerName</span></span>
<span data-ttu-id="d0c21-129">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d0c21-129">The name of the server.</span></span>

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

### <span data-ttu-id="d0c21-130">-Source</span><span class="sxs-lookup"><span data-stu-id="d0c21-130">-Source</span></span>
<span data-ttu-id="d0c21-131">A origem do valor de atualização.</span><span class="sxs-lookup"><span data-stu-id="d0c21-131">The source of the updating value.</span></span>
<span data-ttu-id="d0c21-132">O valor padrão é substituição de usuário</span><span class="sxs-lookup"><span data-stu-id="d0c21-132">The default value is user-override</span></span>

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

### <span data-ttu-id="d0c21-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d0c21-133">-SubscriptionId</span></span>
<span data-ttu-id="d0c21-134">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d0c21-134">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d0c21-135">-Value</span><span class="sxs-lookup"><span data-stu-id="d0c21-135">-Value</span></span>
<span data-ttu-id="d0c21-136">Valor da configuração.</span><span class="sxs-lookup"><span data-stu-id="d0c21-136">Value of the configuration.</span></span>

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

### <span data-ttu-id="d0c21-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0c21-137">-Confirm</span></span>
<span data-ttu-id="d0c21-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0c21-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0c21-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0c21-139">-WhatIf</span></span>
<span data-ttu-id="d0c21-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d0c21-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0c21-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d0c21-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0c21-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c21-142">CommonParameters</span></span>
<span data-ttu-id="d0c21-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0c21-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c21-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0c21-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c21-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0c21-145">INPUTS</span></span>

### <span data-ttu-id="d0c21-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d0c21-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d0c21-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d0c21-147">OUTPUTS</span></span>

### <span data-ttu-id="d0c21-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="d0c21-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="d0c21-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="d0c21-149">NOTES</span></span>

<span data-ttu-id="d0c21-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d0c21-150">ALIASES</span></span>

<span data-ttu-id="d0c21-151">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="d0c21-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d0c21-152">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d0c21-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d0c21-153">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d0c21-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d0c21-154">INPUTOBJECT <IMySqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="d0c21-154">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d0c21-155">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="d0c21-155">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d0c21-156">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d0c21-156">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d0c21-157">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="d0c21-157">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d0c21-158">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d0c21-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d0c21-159">`[KeyName <String>]`: O nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="d0c21-159">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="d0c21-160">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="d0c21-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d0c21-161">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d0c21-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d0c21-162">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d0c21-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="d0c21-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="d0c21-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d0c21-164">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d0c21-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d0c21-165">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d0c21-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d0c21-166">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d0c21-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d0c21-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0c21-167">RELATED LINKS</span></span>

