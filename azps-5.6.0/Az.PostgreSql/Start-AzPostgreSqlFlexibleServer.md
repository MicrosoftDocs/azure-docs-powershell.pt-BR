---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/start-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Start-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Start-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 52ce5b9126fdaae430878c14873a97b0da8737d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885583"
---
# <span data-ttu-id="cccaf-101">Start-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="cccaf-101">Start-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="cccaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cccaf-102">SYNOPSIS</span></span>
<span data-ttu-id="cccaf-103">Inicia um servidor.</span><span class="sxs-lookup"><span data-stu-id="cccaf-103">Starts a server.</span></span>

## <span data-ttu-id="cccaf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cccaf-104">SYNTAX</span></span>

### <span data-ttu-id="cccaf-105">Iniciar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cccaf-105">Start (Default)</span></span>
```
Start-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cccaf-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cccaf-106">StartViaIdentity</span></span>
```
Start-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cccaf-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cccaf-107">DESCRIPTION</span></span>
<span data-ttu-id="cccaf-108">Inicia um servidor.</span><span class="sxs-lookup"><span data-stu-id="cccaf-108">Starts a server.</span></span>

## <span data-ttu-id="cccaf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cccaf-109">EXAMPLES</span></span>

### <span data-ttu-id="cccaf-110">Exemplo 1: Iniciar o servidor pelo nome do recurso</span><span class="sxs-lookup"><span data-stu-id="cccaf-110">Example 1: Start the server by resource name</span></span>
```powershell
PS C:\> Start-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test
```

<span data-ttu-id="cccaf-111">Iniciar o servidor pelo nome</span><span class="sxs-lookup"><span data-stu-id="cccaf-111">Start the server by name</span></span>

### <span data-ttu-id="cccaf-112">Exemplo 2: Iniciar o servidor por identidade</span><span class="sxs-lookup"><span data-stu-id="cccaf-112">Example 2: Start the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/start"
PS C:\> Start-AzPostgreSqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="cccaf-113">Iniciar o servidor por identidade</span><span class="sxs-lookup"><span data-stu-id="cccaf-113">Start the server by identity</span></span>

## <span data-ttu-id="cccaf-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cccaf-114">PARAMETERS</span></span>

### <span data-ttu-id="cccaf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cccaf-115">-AsJob</span></span>
<span data-ttu-id="cccaf-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="cccaf-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cccaf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cccaf-117">-DefaultProfile</span></span>
<span data-ttu-id="cccaf-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cccaf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cccaf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cccaf-119">-InputObject</span></span>
<span data-ttu-id="cccaf-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cccaf-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cccaf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cccaf-121">-Name</span></span>
<span data-ttu-id="cccaf-122">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="cccaf-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cccaf-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cccaf-123">-NoWait</span></span>
<span data-ttu-id="cccaf-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="cccaf-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cccaf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cccaf-125">-PassThru</span></span>
<span data-ttu-id="cccaf-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="cccaf-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cccaf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cccaf-127">-ResourceGroupName</span></span>
<span data-ttu-id="cccaf-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cccaf-128">The name of the resource group.</span></span>
<span data-ttu-id="cccaf-129">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cccaf-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cccaf-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cccaf-130">-SubscriptionId</span></span>
<span data-ttu-id="cccaf-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="cccaf-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cccaf-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cccaf-132">-Confirm</span></span>
<span data-ttu-id="cccaf-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cccaf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cccaf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cccaf-134">-WhatIf</span></span>
<span data-ttu-id="cccaf-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cccaf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cccaf-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cccaf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cccaf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cccaf-137">CommonParameters</span></span>
<span data-ttu-id="cccaf-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cccaf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cccaf-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cccaf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cccaf-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cccaf-140">INPUTS</span></span>

### <span data-ttu-id="cccaf-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="cccaf-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="cccaf-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cccaf-142">OUTPUTS</span></span>

### <span data-ttu-id="cccaf-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cccaf-143">System.Boolean</span></span>

## <span data-ttu-id="cccaf-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="cccaf-144">NOTES</span></span>

<span data-ttu-id="cccaf-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cccaf-145">ALIASES</span></span>

<span data-ttu-id="cccaf-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="cccaf-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cccaf-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="cccaf-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cccaf-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cccaf-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cccaf-149">INPUTOBJECT <IPostgreSqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="cccaf-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cccaf-150">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="cccaf-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="cccaf-151">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cccaf-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="cccaf-152">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="cccaf-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="cccaf-153">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="cccaf-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cccaf-154">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="cccaf-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="cccaf-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cccaf-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cccaf-156">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cccaf-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="cccaf-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="cccaf-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="cccaf-158">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="cccaf-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="cccaf-159">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="cccaf-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cccaf-160">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="cccaf-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="cccaf-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cccaf-161">RELATED LINKS</span></span>

