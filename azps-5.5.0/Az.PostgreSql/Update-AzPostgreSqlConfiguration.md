---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: e1b0ea3d07a7504e75f8bd6143820c52e73d9cf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112721"
---
# <span data-ttu-id="247a9-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="247a9-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="247a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="247a9-102">SYNOPSIS</span></span>
<span data-ttu-id="247a9-103">Atualiza uma configuração de um servidor.</span><span class="sxs-lookup"><span data-stu-id="247a9-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="247a9-104">Use Update-AzPostgreSqlServer em vez disso, se quiser atualizar o AdministratorLoginPassword, sku etc.</span><span class="sxs-lookup"><span data-stu-id="247a9-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="247a9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="247a9-105">SYNTAX</span></span>

### <span data-ttu-id="247a9-106">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="247a9-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="247a9-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="247a9-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="247a9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="247a9-108">DESCRIPTION</span></span>
<span data-ttu-id="247a9-109">Atualiza uma configuração de um servidor.</span><span class="sxs-lookup"><span data-stu-id="247a9-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="247a9-110">Use Update-AzPostgreSqlServer em vez disso, se quiser atualizar o AdministratorLoginPassword, sku etc.</span><span class="sxs-lookup"><span data-stu-id="247a9-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="247a9-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="247a9-111">EXAMPLES</span></span>

### <span data-ttu-id="247a9-112">Exemplo 1: Atualizar configuração PostgreSql por nome</span><span class="sxs-lookup"><span data-stu-id="247a9-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="247a9-113">Este cmdlet atualiza a configuração PostgreSql por nome.</span><span class="sxs-lookup"><span data-stu-id="247a9-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="247a9-114">Exemplo 2: Atualizar configuração PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="247a9-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="247a9-115">Esses cmdlets atualizam a configuração PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="247a9-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="247a9-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="247a9-116">PARAMETERS</span></span>

### <span data-ttu-id="247a9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="247a9-117">-AsJob</span></span>
<span data-ttu-id="247a9-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="247a9-118">Run the command as a job</span></span>

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

### <span data-ttu-id="247a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="247a9-119">-DefaultProfile</span></span>
<span data-ttu-id="247a9-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="247a9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="247a9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="247a9-121">-InputObject</span></span>
<span data-ttu-id="247a9-122">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="247a9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="247a9-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="247a9-123">-Name</span></span>
<span data-ttu-id="247a9-124">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="247a9-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="247a9-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="247a9-125">-NoWait</span></span>
<span data-ttu-id="247a9-126">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="247a9-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="247a9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="247a9-127">-ResourceGroupName</span></span>
<span data-ttu-id="247a9-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="247a9-128">The name of the resource group.</span></span>
<span data-ttu-id="247a9-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="247a9-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="247a9-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="247a9-130">-ServerName</span></span>
<span data-ttu-id="247a9-131">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="247a9-131">The name of the server.</span></span>

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

### <span data-ttu-id="247a9-132">-Origem</span><span class="sxs-lookup"><span data-stu-id="247a9-132">-Source</span></span>
<span data-ttu-id="247a9-133">Origem da configuração.</span><span class="sxs-lookup"><span data-stu-id="247a9-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="247a9-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="247a9-134">-SubscriptionId</span></span>
<span data-ttu-id="247a9-135">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="247a9-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="247a9-136">-Valor</span><span class="sxs-lookup"><span data-stu-id="247a9-136">-Value</span></span>
<span data-ttu-id="247a9-137">Valor da configuração.</span><span class="sxs-lookup"><span data-stu-id="247a9-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="247a9-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="247a9-138">-Confirm</span></span>
<span data-ttu-id="247a9-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="247a9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="247a9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="247a9-140">-WhatIf</span></span>
<span data-ttu-id="247a9-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="247a9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="247a9-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="247a9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="247a9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="247a9-143">CommonParameters</span></span>
<span data-ttu-id="247a9-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="247a9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="247a9-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="247a9-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="247a9-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="247a9-146">INPUTS</span></span>

### <span data-ttu-id="247a9-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="247a9-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="247a9-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="247a9-148">OUTPUTS</span></span>

### <span data-ttu-id="247a9-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="247a9-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="247a9-150">Notas</span><span class="sxs-lookup"><span data-stu-id="247a9-150">NOTES</span></span>

<span data-ttu-id="247a9-151">Aliases</span><span class="sxs-lookup"><span data-stu-id="247a9-151">ALIASES</span></span>

<span data-ttu-id="247a9-152">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="247a9-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="247a9-153">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="247a9-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="247a9-154">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="247a9-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="247a9-155">INPUTOBJECT: <IPostgreSqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="247a9-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="247a9-156">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="247a9-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="247a9-157">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="247a9-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="247a9-158">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="247a9-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="247a9-159">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="247a9-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="247a9-160">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="247a9-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="247a9-161">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="247a9-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="247a9-162">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="247a9-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="247a9-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="247a9-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="247a9-164">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="247a9-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="247a9-165">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="247a9-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="247a9-166">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="247a9-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="247a9-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="247a9-167">RELATED LINKS</span></span>

