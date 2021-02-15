---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restart-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlFlexibleServer.md
ms.openlocfilehash: dacaab524db0403d4f7c1ac2df9b215e920afa18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117503"
---
# <span data-ttu-id="a86f3-101">Restart-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="a86f3-101">Restart-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="a86f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a86f3-102">SYNOPSIS</span></span>
<span data-ttu-id="a86f3-103">Reinicia um servidor.</span><span class="sxs-lookup"><span data-stu-id="a86f3-103">Restarts a server.</span></span>

## <span data-ttu-id="a86f3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a86f3-104">SYNTAX</span></span>

### <span data-ttu-id="a86f3-105">Reiniciar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a86f3-105">Restart (Default)</span></span>
```
Restart-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a86f3-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a86f3-106">RestartViaIdentity</span></span>
```
Restart-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a86f3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a86f3-107">DESCRIPTION</span></span>
<span data-ttu-id="a86f3-108">Reinicia um servidor.</span><span class="sxs-lookup"><span data-stu-id="a86f3-108">Restarts a server.</span></span>

## <span data-ttu-id="a86f3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a86f3-109">EXAMPLES</span></span>

### <span data-ttu-id="a86f3-110">Exemplo 1: Reiniciar o servidor por nome do recurso</span><span class="sxs-lookup"><span data-stu-id="a86f3-110">Example 1: Restart the server by resource name</span></span>
```powershell
PS C:\> Restart-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="a86f3-111">Reiniciar o servidor por nome</span><span class="sxs-lookup"><span data-stu-id="a86f3-111">Restart the server by name</span></span>

### <span data-ttu-id="a86f3-112">Exemplo 2: Reiniciar o servidor por identidade</span><span class="sxs-lookup"><span data-stu-id="a86f3-112">Example 2: Restart the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/restart"
PS C:\> Restart-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="a86f3-113">Reiniciar o servidor por identidade</span><span class="sxs-lookup"><span data-stu-id="a86f3-113">Restart the server by identity</span></span>

## <span data-ttu-id="a86f3-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a86f3-114">PARAMETERS</span></span>

### <span data-ttu-id="a86f3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a86f3-115">-AsJob</span></span>
<span data-ttu-id="a86f3-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="a86f3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a86f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a86f3-117">-DefaultProfile</span></span>
<span data-ttu-id="a86f3-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a86f3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a86f3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a86f3-119">-InputObject</span></span>
<span data-ttu-id="a86f3-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="a86f3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a86f3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a86f3-121">-Name</span></span>
<span data-ttu-id="a86f3-122">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a86f3-122">The name of the server.</span></span>

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

### <span data-ttu-id="a86f3-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a86f3-123">-NoWait</span></span>
<span data-ttu-id="a86f3-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="a86f3-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a86f3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a86f3-125">-PassThru</span></span>
<span data-ttu-id="a86f3-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="a86f3-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a86f3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a86f3-127">-ResourceGroupName</span></span>
<span data-ttu-id="a86f3-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a86f3-128">The name of the resource group.</span></span>
<span data-ttu-id="a86f3-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a86f3-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a86f3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a86f3-130">-SubscriptionId</span></span>
<span data-ttu-id="a86f3-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a86f3-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a86f3-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a86f3-132">-Confirm</span></span>
<span data-ttu-id="a86f3-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a86f3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a86f3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a86f3-134">-WhatIf</span></span>
<span data-ttu-id="a86f3-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a86f3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a86f3-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a86f3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a86f3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a86f3-137">CommonParameters</span></span>
<span data-ttu-id="a86f3-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a86f3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a86f3-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a86f3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a86f3-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="a86f3-140">INPUTS</span></span>

### <span data-ttu-id="a86f3-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a86f3-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="a86f3-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="a86f3-142">OUTPUTS</span></span>

### <span data-ttu-id="a86f3-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a86f3-143">System.Boolean</span></span>

## <span data-ttu-id="a86f3-144">Notas</span><span class="sxs-lookup"><span data-stu-id="a86f3-144">NOTES</span></span>

<span data-ttu-id="a86f3-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="a86f3-145">ALIASES</span></span>

<span data-ttu-id="a86f3-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="a86f3-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a86f3-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a86f3-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a86f3-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a86f3-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a86f3-149">INPUTOBJECT: <IMySqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="a86f3-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a86f3-150">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="a86f3-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a86f3-151">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a86f3-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a86f3-152">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="a86f3-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a86f3-153">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="a86f3-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a86f3-154">`[KeyName <String>]`: o nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="a86f3-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="a86f3-155">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="a86f3-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a86f3-156">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a86f3-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a86f3-157">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a86f3-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="a86f3-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="a86f3-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a86f3-159">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a86f3-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a86f3-160">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a86f3-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a86f3-161">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a86f3-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a86f3-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a86f3-162">RELATED LINKS</span></span>

