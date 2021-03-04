---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/remove-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: b4d9553fe72c1179d82645606515165a3104abf2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885596"
---
# <span data-ttu-id="68a9a-101">Remove-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="68a9a-101">Remove-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="68a9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="68a9a-103">Exclui um servidor.</span><span class="sxs-lookup"><span data-stu-id="68a9a-103">Deletes a server.</span></span>

## <span data-ttu-id="68a9a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="68a9a-104">SYNTAX</span></span>

### <span data-ttu-id="68a9a-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="68a9a-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="68a9a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="68a9a-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="68a9a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="68a9a-107">DESCRIPTION</span></span>
<span data-ttu-id="68a9a-108">Exclui um servidor.</span><span class="sxs-lookup"><span data-stu-id="68a9a-108">Deletes a server.</span></span>

## <span data-ttu-id="68a9a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68a9a-109">EXAMPLES</span></span>

### <span data-ttu-id="68a9a-110">Exemplo 1: Remover servidor PostgreSql por resourceGroup e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="68a9a-110">Example 1: Remove PostgreSql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test

```

<span data-ttu-id="68a9a-111">Este cmdlet remove o servidor PostgreSql por resourceGroup e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="68a9a-111">This cmdlet removes PostgreSql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="68a9a-112">Exemplo 2: Remover servidor PostgreSql por identidade</span><span class="sxs-lookup"><span data-stu-id="68a9a-112">Example 2: Remove PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test"
PS C:\> Remove-AzPostgreSqlFlexibleServer -InputObject $ID
 
```

<span data-ttu-id="68a9a-113">Esses cmdlets removem o servidor PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="68a9a-113">These cmdlets remove PostgreSql server by identity.</span></span>

## <span data-ttu-id="68a9a-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="68a9a-114">PARAMETERS</span></span>

### <span data-ttu-id="68a9a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68a9a-115">-AsJob</span></span>
<span data-ttu-id="68a9a-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="68a9a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="68a9a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a9a-117">-DefaultProfile</span></span>
<span data-ttu-id="68a9a-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68a9a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68a9a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68a9a-119">-InputObject</span></span>
<span data-ttu-id="68a9a-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="68a9a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="68a9a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="68a9a-121">-Name</span></span>
<span data-ttu-id="68a9a-122">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="68a9a-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a9a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="68a9a-123">-NoWait</span></span>
<span data-ttu-id="68a9a-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="68a9a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="68a9a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68a9a-125">-PassThru</span></span>
<span data-ttu-id="68a9a-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="68a9a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="68a9a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68a9a-127">-ResourceGroupName</span></span>
<span data-ttu-id="68a9a-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="68a9a-128">The name of the resource group.</span></span>
<span data-ttu-id="68a9a-129">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="68a9a-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="68a9a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68a9a-130">-SubscriptionId</span></span>
<span data-ttu-id="68a9a-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="68a9a-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="68a9a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68a9a-132">-Confirm</span></span>
<span data-ttu-id="68a9a-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68a9a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68a9a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68a9a-134">-WhatIf</span></span>
<span data-ttu-id="68a9a-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="68a9a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68a9a-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="68a9a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68a9a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a9a-137">CommonParameters</span></span>
<span data-ttu-id="68a9a-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68a9a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a9a-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68a9a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a9a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68a9a-140">INPUTS</span></span>

### <span data-ttu-id="68a9a-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="68a9a-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="68a9a-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="68a9a-142">OUTPUTS</span></span>

### <span data-ttu-id="68a9a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="68a9a-143">System.Boolean</span></span>

## <span data-ttu-id="68a9a-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="68a9a-144">NOTES</span></span>

<span data-ttu-id="68a9a-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="68a9a-145">ALIASES</span></span>

<span data-ttu-id="68a9a-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="68a9a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="68a9a-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="68a9a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="68a9a-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="68a9a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="68a9a-149">INPUTOBJECT <IPostgreSqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="68a9a-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="68a9a-150">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="68a9a-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="68a9a-151">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="68a9a-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="68a9a-152">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="68a9a-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="68a9a-153">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="68a9a-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="68a9a-154">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="68a9a-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="68a9a-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="68a9a-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="68a9a-156">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="68a9a-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="68a9a-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="68a9a-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="68a9a-158">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="68a9a-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="68a9a-159">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="68a9a-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="68a9a-160">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="68a9a-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="68a9a-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68a9a-161">RELATED LINKS</span></span>

