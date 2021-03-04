---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/remove-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: c2bb8923a9844563f128866c324688d23413a641
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885590"
---
# <span data-ttu-id="97566-101">Remove-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="97566-101">Remove-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="97566-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97566-102">SYNOPSIS</span></span>
<span data-ttu-id="97566-103">Exclui uma regra de firewall de servidor PostgreSQL.</span><span class="sxs-lookup"><span data-stu-id="97566-103">Deletes a PostgreSQL server firewall rule.</span></span>

## <span data-ttu-id="97566-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="97566-104">SYNTAX</span></span>

### <span data-ttu-id="97566-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="97566-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="97566-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="97566-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="97566-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="97566-107">DESCRIPTION</span></span>
<span data-ttu-id="97566-108">Exclui uma regra de firewall de servidor PostgreSQL.</span><span class="sxs-lookup"><span data-stu-id="97566-108">Deletes a PostgreSQL server firewall rule.</span></span>

## <span data-ttu-id="97566-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97566-109">EXAMPLES</span></span>

### <span data-ttu-id="97566-110">Exemplo 1: Remover Regra de Firewall PostgreSql pelo nome</span><span class="sxs-lookup"><span data-stu-id="97566-110">Example 1: Remove PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFlexibleServerFirewallRule -Name firewall-rule-test -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

```

<span data-ttu-id="97566-111">Este cmdlet remove a Regra de Firewall PostgreSql pelo nome.</span><span class="sxs-lookup"><span data-stu-id="97566-111">This cmdlet removes PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="97566-112">Exemplo 2: Remover Regra de Firewall PostgreSql por identidade</span><span class="sxs-lookup"><span data-stu-id="97566-112">Example 2: Remove PostgreSql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/firewallRules/firewall-rule-test"
PS C:\> Remove-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID
 
```

<span data-ttu-id="97566-113">Esses cmdlets removem a Regra de Firewall PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="97566-113">These cmdlets remove PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="97566-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="97566-114">PARAMETERS</span></span>

### <span data-ttu-id="97566-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97566-115">-AsJob</span></span>
<span data-ttu-id="97566-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="97566-116">Run the command as a job</span></span>

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

### <span data-ttu-id="97566-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97566-117">-DefaultProfile</span></span>
<span data-ttu-id="97566-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97566-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97566-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97566-119">-InputObject</span></span>
<span data-ttu-id="97566-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="97566-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97566-121">-Name</span><span class="sxs-lookup"><span data-stu-id="97566-121">-Name</span></span>
<span data-ttu-id="97566-122">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="97566-122">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97566-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="97566-123">-NoWait</span></span>
<span data-ttu-id="97566-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="97566-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="97566-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97566-125">-PassThru</span></span>
<span data-ttu-id="97566-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="97566-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="97566-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97566-127">-ResourceGroupName</span></span>
<span data-ttu-id="97566-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="97566-128">The name of the resource group.</span></span>
<span data-ttu-id="97566-129">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="97566-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97566-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="97566-130">-ServerName</span></span>
<span data-ttu-id="97566-131">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="97566-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97566-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97566-132">-SubscriptionId</span></span>
<span data-ttu-id="97566-133">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="97566-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97566-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97566-134">-Confirm</span></span>
<span data-ttu-id="97566-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97566-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97566-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97566-136">-WhatIf</span></span>
<span data-ttu-id="97566-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97566-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97566-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97566-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97566-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97566-139">CommonParameters</span></span>
<span data-ttu-id="97566-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97566-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97566-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97566-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97566-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97566-142">INPUTS</span></span>

### <span data-ttu-id="97566-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="97566-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="97566-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="97566-144">OUTPUTS</span></span>

### <span data-ttu-id="97566-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="97566-145">System.Boolean</span></span>

## <span data-ttu-id="97566-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="97566-146">NOTES</span></span>

<span data-ttu-id="97566-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="97566-147">ALIASES</span></span>

<span data-ttu-id="97566-148">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="97566-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="97566-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="97566-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97566-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97566-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="97566-151">INPUTOBJECT <IPostgreSqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="97566-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97566-152">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="97566-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="97566-153">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="97566-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="97566-154">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="97566-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="97566-155">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="97566-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97566-156">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="97566-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="97566-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="97566-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="97566-158">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="97566-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="97566-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="97566-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="97566-160">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="97566-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="97566-161">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="97566-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="97566-162">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="97566-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="97566-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97566-163">RELATED LINKS</span></span>

