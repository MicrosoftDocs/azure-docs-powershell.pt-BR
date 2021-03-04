---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/remove-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: ef3f9f519e63a6d21ef245fdd0578aec2736803f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889902"
---
# <span data-ttu-id="3a166-101">Remove-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3a166-101">Remove-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="3a166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a166-102">SYNOPSIS</span></span>
<span data-ttu-id="3a166-103">Exclui uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="3a166-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="3a166-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3a166-104">SYNTAX</span></span>

### <span data-ttu-id="3a166-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3a166-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3a166-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3a166-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3a166-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3a166-107">DESCRIPTION</span></span>
<span data-ttu-id="3a166-108">Exclui uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="3a166-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="3a166-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a166-109">EXAMPLES</span></span>

### <span data-ttu-id="3a166-110">Exemplo 1: Remover Regra de Firewall PostgreSql pelo nome</span><span class="sxs-lookup"><span data-stu-id="3a166-110">Example 1: Remove PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="3a166-111">Este cmdlet remove a Regra de Firewall PostgreSql pelo nome.</span><span class="sxs-lookup"><span data-stu-id="3a166-111">This cmdlet removes PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="3a166-112">Exemplo 2: Remover Regra de Firewall PostgreSql por identidade</span><span class="sxs-lookup"><span data-stu-id="3a166-112">Example 2: Remove PostgreSql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Remove-AzPostgreSqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="3a166-113">Esses cmdlets removem a Regra de Firewall PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="3a166-113">These cmdlets remove PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="3a166-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3a166-114">PARAMETERS</span></span>

### <span data-ttu-id="3a166-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a166-115">-AsJob</span></span>
<span data-ttu-id="3a166-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="3a166-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3a166-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a166-117">-DefaultProfile</span></span>
<span data-ttu-id="3a166-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a166-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a166-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a166-119">-InputObject</span></span>
<span data-ttu-id="3a166-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3a166-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3a166-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3a166-121">-Name</span></span>
<span data-ttu-id="3a166-122">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="3a166-122">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="3a166-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3a166-123">-NoWait</span></span>
<span data-ttu-id="3a166-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="3a166-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3a166-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a166-125">-PassThru</span></span>
<span data-ttu-id="3a166-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="3a166-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3a166-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a166-127">-ResourceGroupName</span></span>
<span data-ttu-id="3a166-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a166-128">The name of the resource group.</span></span>
<span data-ttu-id="3a166-129">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3a166-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3a166-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3a166-130">-ServerName</span></span>
<span data-ttu-id="3a166-131">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="3a166-131">The name of the server.</span></span>

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

### <span data-ttu-id="3a166-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a166-132">-SubscriptionId</span></span>
<span data-ttu-id="3a166-133">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="3a166-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3a166-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a166-134">-Confirm</span></span>
<span data-ttu-id="3a166-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a166-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a166-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a166-136">-WhatIf</span></span>
<span data-ttu-id="3a166-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a166-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a166-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a166-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a166-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a166-139">CommonParameters</span></span>
<span data-ttu-id="3a166-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a166-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a166-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a166-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a166-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a166-142">INPUTS</span></span>

### <span data-ttu-id="3a166-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3a166-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="3a166-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3a166-144">OUTPUTS</span></span>

### <span data-ttu-id="3a166-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a166-145">System.Boolean</span></span>

## <span data-ttu-id="3a166-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="3a166-146">NOTES</span></span>

<span data-ttu-id="3a166-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3a166-147">ALIASES</span></span>

<span data-ttu-id="3a166-148">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="3a166-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3a166-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="3a166-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a166-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3a166-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3a166-151">INPUTOBJECT <IPostgreSqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="3a166-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3a166-152">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="3a166-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3a166-153">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3a166-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3a166-154">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="3a166-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3a166-155">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="3a166-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3a166-156">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="3a166-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3a166-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a166-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3a166-158">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3a166-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="3a166-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="3a166-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3a166-160">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="3a166-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3a166-161">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="3a166-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3a166-162">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="3a166-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3a166-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a166-163">RELATED LINKS</span></span>

