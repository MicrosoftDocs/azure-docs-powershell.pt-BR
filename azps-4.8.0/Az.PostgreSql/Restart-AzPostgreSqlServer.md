---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
ms.openlocfilehash: aa5e58522aaeb1094ef2a7280b33b45e20fe03fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110345"
---
# <span data-ttu-id="03206-101">Restart-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="03206-101">Restart-AzPostgreSqlServer</span></span>

## <span data-ttu-id="03206-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03206-102">SYNOPSIS</span></span>
<span data-ttu-id="03206-103">Reinicia um servidor.</span><span class="sxs-lookup"><span data-stu-id="03206-103">Restarts a server.</span></span>

## <span data-ttu-id="03206-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03206-104">SYNTAX</span></span>

### <span data-ttu-id="03206-105">Reiniciar (padrão)</span><span class="sxs-lookup"><span data-stu-id="03206-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="03206-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="03206-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="03206-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="03206-107">DESCRIPTION</span></span>
<span data-ttu-id="03206-108">Reinicia um servidor.</span><span class="sxs-lookup"><span data-stu-id="03206-108">Restarts a server.</span></span>

## <span data-ttu-id="03206-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03206-109">EXAMPLES</span></span>

### <span data-ttu-id="03206-110">Exemplo 1: reiniciar o servidor PostgreSql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="03206-110">Example 1: Restart PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="03206-111">Este cmdlet reinicia o servidor PostgreSql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="03206-111">This cmdlet restarts PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="03206-112">Exemplo 2: reiniciar o servidor PostgreSql por identidade</span><span class="sxs-lookup"><span data-stu-id="03206-112">Example 2: Restart PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/restart"
PS C:\> Restart-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="03206-113">Esses cmdlets reiniciam o servidor PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="03206-113">These cmdlets restart PostgreSql server by identity.</span></span>

## <span data-ttu-id="03206-114">OS</span><span class="sxs-lookup"><span data-stu-id="03206-114">PARAMETERS</span></span>

### <span data-ttu-id="03206-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03206-115">-AsJob</span></span>
<span data-ttu-id="03206-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="03206-116">Run the command as a job</span></span>

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

### <span data-ttu-id="03206-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03206-117">-DefaultProfile</span></span>
<span data-ttu-id="03206-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03206-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03206-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03206-119">-InputObject</span></span>
<span data-ttu-id="03206-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="03206-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="03206-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="03206-121">-Name</span></span>
<span data-ttu-id="03206-122">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="03206-122">The name of the server.</span></span>

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

### <span data-ttu-id="03206-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="03206-123">-NoWait</span></span>
<span data-ttu-id="03206-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="03206-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="03206-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03206-125">-PassThru</span></span>
<span data-ttu-id="03206-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="03206-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="03206-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03206-127">-ResourceGroupName</span></span>
<span data-ttu-id="03206-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="03206-128">The name of the resource group.</span></span>
<span data-ttu-id="03206-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="03206-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="03206-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03206-130">-SubscriptionId</span></span>
<span data-ttu-id="03206-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="03206-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="03206-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="03206-132">-Confirm</span></span>
<span data-ttu-id="03206-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03206-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03206-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03206-134">-WhatIf</span></span>
<span data-ttu-id="03206-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="03206-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03206-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="03206-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03206-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03206-137">CommonParameters</span></span>
<span data-ttu-id="03206-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03206-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03206-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03206-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03206-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="03206-140">INPUTS</span></span>

### <span data-ttu-id="03206-141">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="03206-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="03206-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="03206-142">OUTPUTS</span></span>

### <span data-ttu-id="03206-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03206-143">System.Boolean</span></span>

## <span data-ttu-id="03206-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="03206-144">NOTES</span></span>

<span data-ttu-id="03206-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="03206-145">ALIASES</span></span>

<span data-ttu-id="03206-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="03206-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="03206-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="03206-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="03206-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="03206-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="03206-149">INPUTobject <IPostgreSqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="03206-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="03206-150">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="03206-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="03206-151">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="03206-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="03206-152">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="03206-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="03206-153">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="03206-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="03206-154">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="03206-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="03206-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="03206-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="03206-156">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="03206-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="03206-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="03206-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="03206-158">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="03206-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="03206-159">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="03206-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="03206-160">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="03206-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="03206-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03206-161">RELATED LINKS</span></span>

