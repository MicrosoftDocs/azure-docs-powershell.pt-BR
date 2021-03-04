---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/restart-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 8e969551724a4965d17ce34e3b18c794705b764f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885588"
---
# <span data-ttu-id="fd57e-101">Restart-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="fd57e-101">Restart-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="fd57e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd57e-102">SYNOPSIS</span></span>
<span data-ttu-id="fd57e-103">Reinicia um servidor.</span><span class="sxs-lookup"><span data-stu-id="fd57e-103">Restarts a server.</span></span>

## <span data-ttu-id="fd57e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fd57e-104">SYNTAX</span></span>

### <span data-ttu-id="fd57e-105">Reiniciar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fd57e-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fd57e-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fd57e-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fd57e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fd57e-107">DESCRIPTION</span></span>
<span data-ttu-id="fd57e-108">Reinicia um servidor.</span><span class="sxs-lookup"><span data-stu-id="fd57e-108">Restarts a server.</span></span>

## <span data-ttu-id="fd57e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd57e-109">EXAMPLES</span></span>

### <span data-ttu-id="fd57e-110">Exemplo 1: Reiniciar o servidor pelo nome do recurso</span><span class="sxs-lookup"><span data-stu-id="fd57e-110">Example 1: Restart the server by resource name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test
```

<span data-ttu-id="fd57e-111">Reiniciar o servidor pelo nome</span><span class="sxs-lookup"><span data-stu-id="fd57e-111">Restart the server by name</span></span>

### <span data-ttu-id="fd57e-112">Exemplo 2: Reiniciar o servidor por identidade</span><span class="sxs-lookup"><span data-stu-id="fd57e-112">Example 2: Restart the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/restart"
PS C:\> Restart-AzPostgreSqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="fd57e-113">Reiniciar o servidor por identidade</span><span class="sxs-lookup"><span data-stu-id="fd57e-113">Restart the server by identity</span></span>

## <span data-ttu-id="fd57e-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fd57e-114">PARAMETERS</span></span>

### <span data-ttu-id="fd57e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd57e-115">-AsJob</span></span>
<span data-ttu-id="fd57e-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="fd57e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fd57e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd57e-117">-DefaultProfile</span></span>
<span data-ttu-id="fd57e-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd57e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd57e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd57e-119">-InputObject</span></span>
<span data-ttu-id="fd57e-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fd57e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd57e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fd57e-121">-Name</span></span>
<span data-ttu-id="fd57e-122">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="fd57e-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd57e-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fd57e-123">-NoWait</span></span>
<span data-ttu-id="fd57e-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="fd57e-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fd57e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd57e-125">-PassThru</span></span>
<span data-ttu-id="fd57e-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="fd57e-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fd57e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd57e-127">-ResourceGroupName</span></span>
<span data-ttu-id="fd57e-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fd57e-128">The name of the resource group.</span></span>
<span data-ttu-id="fd57e-129">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fd57e-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd57e-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd57e-130">-SubscriptionId</span></span>
<span data-ttu-id="fd57e-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="fd57e-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd57e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd57e-132">-Confirm</span></span>
<span data-ttu-id="fd57e-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd57e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd57e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd57e-134">-WhatIf</span></span>
<span data-ttu-id="fd57e-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fd57e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd57e-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd57e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd57e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd57e-137">CommonParameters</span></span>
<span data-ttu-id="fd57e-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd57e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd57e-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd57e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd57e-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd57e-140">INPUTS</span></span>

### <span data-ttu-id="fd57e-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="fd57e-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="fd57e-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fd57e-142">OUTPUTS</span></span>

### <span data-ttu-id="fd57e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd57e-143">System.Boolean</span></span>

## <span data-ttu-id="fd57e-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="fd57e-144">NOTES</span></span>

<span data-ttu-id="fd57e-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fd57e-145">ALIASES</span></span>

<span data-ttu-id="fd57e-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="fd57e-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fd57e-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="fd57e-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fd57e-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fd57e-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fd57e-149">INPUTOBJECT <IPostgreSqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="fd57e-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fd57e-150">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="fd57e-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fd57e-151">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fd57e-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fd57e-152">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="fd57e-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fd57e-153">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="fd57e-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fd57e-154">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="fd57e-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fd57e-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fd57e-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fd57e-156">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fd57e-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="fd57e-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="fd57e-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fd57e-158">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="fd57e-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fd57e-159">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="fd57e-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fd57e-160">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fd57e-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fd57e-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd57e-161">RELATED LINKS</span></span>

