---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 9c1a0d2746b40402982f1e904548d92f2776819f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111491"
---
# <span data-ttu-id="fafad-101">Restart-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="fafad-101">Restart-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="fafad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fafad-102">SYNOPSIS</span></span>
<span data-ttu-id="fafad-103">Reinicia um servidor.</span><span class="sxs-lookup"><span data-stu-id="fafad-103">Restarts a server.</span></span>

## <span data-ttu-id="fafad-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fafad-104">SYNTAX</span></span>

### <span data-ttu-id="fafad-105">Reiniciar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fafad-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fafad-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fafad-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fafad-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fafad-107">DESCRIPTION</span></span>
<span data-ttu-id="fafad-108">Reinicia um servidor.</span><span class="sxs-lookup"><span data-stu-id="fafad-108">Restarts a server.</span></span>

## <span data-ttu-id="fafad-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fafad-109">EXAMPLES</span></span>

### <span data-ttu-id="fafad-110">Exemplo 1: Reiniciar o servidor por nome do recurso</span><span class="sxs-lookup"><span data-stu-id="fafad-110">Example 1: Restart the server by resource name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test
```

<span data-ttu-id="fafad-111">Reiniciar o servidor por nome</span><span class="sxs-lookup"><span data-stu-id="fafad-111">Restart the server by name</span></span>

### <span data-ttu-id="fafad-112">Exemplo 2: Reiniciar o servidor por identidade</span><span class="sxs-lookup"><span data-stu-id="fafad-112">Example 2: Restart the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/restart"
PS C:\> Restart-AzPostgreSqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="fafad-113">Reiniciar o servidor por identidade</span><span class="sxs-lookup"><span data-stu-id="fafad-113">Restart the server by identity</span></span>

## <span data-ttu-id="fafad-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fafad-114">PARAMETERS</span></span>

### <span data-ttu-id="fafad-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fafad-115">-AsJob</span></span>
<span data-ttu-id="fafad-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="fafad-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fafad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fafad-117">-DefaultProfile</span></span>
<span data-ttu-id="fafad-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fafad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fafad-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fafad-119">-InputObject</span></span>
<span data-ttu-id="fafad-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="fafad-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fafad-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fafad-121">-Name</span></span>
<span data-ttu-id="fafad-122">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="fafad-122">The name of the server.</span></span>

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

### <span data-ttu-id="fafad-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fafad-123">-NoWait</span></span>
<span data-ttu-id="fafad-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="fafad-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fafad-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fafad-125">-PassThru</span></span>
<span data-ttu-id="fafad-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="fafad-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fafad-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fafad-127">-ResourceGroupName</span></span>
<span data-ttu-id="fafad-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fafad-128">The name of the resource group.</span></span>
<span data-ttu-id="fafad-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fafad-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fafad-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fafad-130">-SubscriptionId</span></span>
<span data-ttu-id="fafad-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="fafad-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fafad-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fafad-132">-Confirm</span></span>
<span data-ttu-id="fafad-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fafad-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fafad-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fafad-134">-WhatIf</span></span>
<span data-ttu-id="fafad-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fafad-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fafad-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fafad-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fafad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fafad-137">CommonParameters</span></span>
<span data-ttu-id="fafad-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fafad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fafad-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fafad-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fafad-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="fafad-140">INPUTS</span></span>

### <span data-ttu-id="fafad-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="fafad-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="fafad-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="fafad-142">OUTPUTS</span></span>

### <span data-ttu-id="fafad-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fafad-143">System.Boolean</span></span>

## <span data-ttu-id="fafad-144">Notas</span><span class="sxs-lookup"><span data-stu-id="fafad-144">NOTES</span></span>

<span data-ttu-id="fafad-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="fafad-145">ALIASES</span></span>

<span data-ttu-id="fafad-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="fafad-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fafad-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="fafad-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fafad-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fafad-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fafad-149">INPUTOBJECT: <IPostgreSqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="fafad-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fafad-150">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="fafad-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fafad-151">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fafad-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fafad-152">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="fafad-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fafad-153">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="fafad-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fafad-154">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="fafad-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fafad-155">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fafad-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fafad-156">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fafad-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="fafad-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="fafad-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fafad-158">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="fafad-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fafad-159">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="fafad-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fafad-160">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fafad-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fafad-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fafad-161">RELATED LINKS</span></span>

