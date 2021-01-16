---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restart-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlServer.md
ms.openlocfilehash: 6af7f506f7757374efa5efc5029b8edc419ce4be
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262674"
---
# <span data-ttu-id="b15f9-101">Restart-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="b15f9-101">Restart-AzMySqlServer</span></span>

## <span data-ttu-id="b15f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b15f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b15f9-103">Reinicia um servidor.</span><span class="sxs-lookup"><span data-stu-id="b15f9-103">Restarts a server.</span></span>

## <span data-ttu-id="b15f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b15f9-104">SYNTAX</span></span>

### <span data-ttu-id="b15f9-105">Reiniciar (padrão)</span><span class="sxs-lookup"><span data-stu-id="b15f9-105">Restart (Default)</span></span>
```
Restart-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b15f9-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b15f9-106">RestartViaIdentity</span></span>
```
Restart-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b15f9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b15f9-107">DESCRIPTION</span></span>
<span data-ttu-id="b15f9-108">Reinicia um servidor.</span><span class="sxs-lookup"><span data-stu-id="b15f9-108">Restarts a server.</span></span>

## <span data-ttu-id="b15f9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b15f9-109">EXAMPLES</span></span>

### <span data-ttu-id="b15f9-110">Exemplo 1: reiniciar o servidor MySql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="b15f9-110">Example 1: Restart MySql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="b15f9-111">Este cmdlet reinicia o MySql Server por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b15f9-111">This cmdlet restarts MySql server by resource group and server name.</span></span>

### <span data-ttu-id="b15f9-112">Exemplo 2: reiniciar o servidor MySql por identidade</span><span class="sxs-lookup"><span data-stu-id="b15f9-112">Example 2: Restart MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/restart"
PS C:\> Restart-AzMySqlServer -InputObject $ID
 
```

<span data-ttu-id="b15f9-113">Esses cmdlets reiniciam o MySql Server por identidade.</span><span class="sxs-lookup"><span data-stu-id="b15f9-113">These cmdlets restart MySql server by identity.</span></span>

## <span data-ttu-id="b15f9-114">OS</span><span class="sxs-lookup"><span data-stu-id="b15f9-114">PARAMETERS</span></span>

### <span data-ttu-id="b15f9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b15f9-115">-AsJob</span></span>
<span data-ttu-id="b15f9-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="b15f9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b15f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b15f9-117">-DefaultProfile</span></span>
<span data-ttu-id="b15f9-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b15f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b15f9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b15f9-119">-InputObject</span></span>
<span data-ttu-id="b15f9-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b15f9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b15f9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b15f9-121">-Name</span></span>
<span data-ttu-id="b15f9-122">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b15f9-122">The name of the server.</span></span>

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

### <span data-ttu-id="b15f9-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b15f9-123">-NoWait</span></span>
<span data-ttu-id="b15f9-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="b15f9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b15f9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b15f9-125">-PassThru</span></span>
<span data-ttu-id="b15f9-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="b15f9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b15f9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b15f9-127">-ResourceGroupName</span></span>
<span data-ttu-id="b15f9-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b15f9-128">The name of the resource group.</span></span>
<span data-ttu-id="b15f9-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b15f9-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b15f9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b15f9-130">-SubscriptionId</span></span>
<span data-ttu-id="b15f9-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b15f9-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b15f9-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b15f9-132">-Confirm</span></span>
<span data-ttu-id="b15f9-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b15f9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b15f9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b15f9-134">-WhatIf</span></span>
<span data-ttu-id="b15f9-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b15f9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b15f9-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b15f9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b15f9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b15f9-137">CommonParameters</span></span>
<span data-ttu-id="b15f9-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b15f9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b15f9-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b15f9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b15f9-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b15f9-140">INPUTS</span></span>

### <span data-ttu-id="b15f9-141">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b15f9-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b15f9-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b15f9-142">OUTPUTS</span></span>

### <span data-ttu-id="b15f9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b15f9-143">System.Boolean</span></span>

## <span data-ttu-id="b15f9-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b15f9-144">NOTES</span></span>

<span data-ttu-id="b15f9-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b15f9-145">ALIASES</span></span>

<span data-ttu-id="b15f9-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="b15f9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b15f9-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b15f9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b15f9-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b15f9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b15f9-149">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="b15f9-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b15f9-150">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="b15f9-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b15f9-151">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b15f9-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b15f9-152">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="b15f9-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b15f9-153">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b15f9-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b15f9-154">`[KeyName <String>]`: O nome da tecla do servidor.</span><span class="sxs-lookup"><span data-stu-id="b15f9-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="b15f9-155">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="b15f9-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b15f9-156">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b15f9-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b15f9-157">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b15f9-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="b15f9-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="b15f9-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b15f9-159">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b15f9-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b15f9-160">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b15f9-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b15f9-161">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b15f9-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b15f9-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b15f9-162">RELATED LINKS</span></span>

