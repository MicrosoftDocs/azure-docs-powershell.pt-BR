---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/stop-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Stop-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Stop-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 02a7d917a63fa7913603a8bc5672f6a41ca8ed2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118196"
---
# <span data-ttu-id="44c52-101">Stop-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="44c52-101">Stop-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="44c52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44c52-102">SYNOPSIS</span></span>
<span data-ttu-id="44c52-103">Interrompe um servidor.</span><span class="sxs-lookup"><span data-stu-id="44c52-103">Stops a server.</span></span>

## <span data-ttu-id="44c52-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44c52-104">SYNTAX</span></span>

### <span data-ttu-id="44c52-105">Parar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="44c52-105">Stop (Default)</span></span>
```
Stop-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="44c52-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="44c52-106">StopViaIdentity</span></span>
```
Stop-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44c52-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="44c52-107">DESCRIPTION</span></span>
<span data-ttu-id="44c52-108">Interrompe um servidor.</span><span class="sxs-lookup"><span data-stu-id="44c52-108">Stops a server.</span></span>

## <span data-ttu-id="44c52-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="44c52-109">EXAMPLES</span></span>

### <span data-ttu-id="44c52-110">Exemplo 1: Parar o servidor por nome do recurso</span><span class="sxs-lookup"><span data-stu-id="44c52-110">Example 1: Stop the server by resource name</span></span>
```powershell
PS C:\> Stop-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test
```

<span data-ttu-id="44c52-111">Parar o servidor por nome</span><span class="sxs-lookup"><span data-stu-id="44c52-111">Stop the server by name</span></span>

### <span data-ttu-id="44c52-112">Exemplo 2: Parar o servidor por identidade</span><span class="sxs-lookup"><span data-stu-id="44c52-112">Example 2: Stop the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/stop"
PS C:\> Stop-AzPostgreSqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="44c52-113">Interromper o servidor por identidade</span><span class="sxs-lookup"><span data-stu-id="44c52-113">Stop the server by identity</span></span>

## <span data-ttu-id="44c52-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44c52-114">PARAMETERS</span></span>

### <span data-ttu-id="44c52-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44c52-115">-AsJob</span></span>
<span data-ttu-id="44c52-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="44c52-116">Run the command as a job</span></span>

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

### <span data-ttu-id="44c52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c52-117">-DefaultProfile</span></span>
<span data-ttu-id="44c52-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44c52-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44c52-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44c52-119">-InputObject</span></span>
<span data-ttu-id="44c52-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="44c52-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44c52-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="44c52-121">-Name</span></span>
<span data-ttu-id="44c52-122">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="44c52-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44c52-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="44c52-123">-NoWait</span></span>
<span data-ttu-id="44c52-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="44c52-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="44c52-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44c52-125">-PassThru</span></span>
<span data-ttu-id="44c52-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="44c52-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="44c52-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44c52-127">-ResourceGroupName</span></span>
<span data-ttu-id="44c52-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44c52-128">The name of the resource group.</span></span>
<span data-ttu-id="44c52-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="44c52-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44c52-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44c52-130">-SubscriptionId</span></span>
<span data-ttu-id="44c52-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="44c52-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44c52-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="44c52-132">-Confirm</span></span>
<span data-ttu-id="44c52-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44c52-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44c52-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44c52-134">-WhatIf</span></span>
<span data-ttu-id="44c52-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="44c52-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44c52-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44c52-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44c52-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c52-137">CommonParameters</span></span>
<span data-ttu-id="44c52-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44c52-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c52-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44c52-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c52-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="44c52-140">INPUTS</span></span>

### <span data-ttu-id="44c52-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="44c52-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="44c52-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="44c52-142">OUTPUTS</span></span>

### <span data-ttu-id="44c52-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="44c52-143">System.Boolean</span></span>

## <span data-ttu-id="44c52-144">Notas</span><span class="sxs-lookup"><span data-stu-id="44c52-144">NOTES</span></span>

<span data-ttu-id="44c52-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="44c52-145">ALIASES</span></span>

<span data-ttu-id="44c52-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="44c52-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="44c52-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="44c52-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44c52-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="44c52-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="44c52-149">INPUTOBJECT: <IPostgreSqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="44c52-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="44c52-150">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="44c52-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="44c52-151">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="44c52-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="44c52-152">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="44c52-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="44c52-153">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="44c52-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="44c52-154">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="44c52-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="44c52-155">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44c52-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="44c52-156">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="44c52-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="44c52-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="44c52-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="44c52-158">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="44c52-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="44c52-159">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="44c52-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="44c52-160">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="44c52-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="44c52-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44c52-161">RELATED LINKS</span></span>

