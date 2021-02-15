---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/stop-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Stop-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Stop-AzMySqlFlexibleServer.md
ms.openlocfilehash: b8be18e0305914eadcd6872a1494a250da3084f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112937"
---
# <span data-ttu-id="d842d-101">Stop-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="d842d-101">Stop-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="d842d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d842d-102">SYNOPSIS</span></span>
<span data-ttu-id="d842d-103">Interrompe um servidor.</span><span class="sxs-lookup"><span data-stu-id="d842d-103">Stops a server.</span></span>

## <span data-ttu-id="d842d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d842d-104">SYNTAX</span></span>

### <span data-ttu-id="d842d-105">Parar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d842d-105">Stop (Default)</span></span>
```
Stop-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d842d-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d842d-106">StopViaIdentity</span></span>
```
Stop-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d842d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d842d-107">DESCRIPTION</span></span>
<span data-ttu-id="d842d-108">Interrompe um servidor.</span><span class="sxs-lookup"><span data-stu-id="d842d-108">Stops a server.</span></span>

## <span data-ttu-id="d842d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d842d-109">EXAMPLES</span></span>

### <span data-ttu-id="d842d-110">Exemplo 1: Parar o servidor por nome do recurso</span><span class="sxs-lookup"><span data-stu-id="d842d-110">Example 1: Stop the server by resource name</span></span>
```powershell
PS C:\> Stop-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="d842d-111">Parar o servidor por nome</span><span class="sxs-lookup"><span data-stu-id="d842d-111">Stop the server by name</span></span>

### <span data-ttu-id="d842d-112">Exemplo 2: Parar o servidor por identidade</span><span class="sxs-lookup"><span data-stu-id="d842d-112">Example 2: Stop the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/stop"
PS C:\> Stop-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="d842d-113">Interromper o servidor por identidade</span><span class="sxs-lookup"><span data-stu-id="d842d-113">Stop the server by identity</span></span>

## <span data-ttu-id="d842d-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d842d-114">PARAMETERS</span></span>

### <span data-ttu-id="d842d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d842d-115">-AsJob</span></span>
<span data-ttu-id="d842d-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="d842d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d842d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d842d-117">-DefaultProfile</span></span>
<span data-ttu-id="d842d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d842d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d842d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d842d-119">-InputObject</span></span>
<span data-ttu-id="d842d-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="d842d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d842d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d842d-121">-Name</span></span>
<span data-ttu-id="d842d-122">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d842d-122">The name of the server.</span></span>

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

### <span data-ttu-id="d842d-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d842d-123">-NoWait</span></span>
<span data-ttu-id="d842d-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="d842d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d842d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d842d-125">-PassThru</span></span>
<span data-ttu-id="d842d-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="d842d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d842d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d842d-127">-ResourceGroupName</span></span>
<span data-ttu-id="d842d-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d842d-128">The name of the resource group.</span></span>
<span data-ttu-id="d842d-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d842d-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d842d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d842d-130">-SubscriptionId</span></span>
<span data-ttu-id="d842d-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d842d-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d842d-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d842d-132">-Confirm</span></span>
<span data-ttu-id="d842d-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d842d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d842d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d842d-134">-WhatIf</span></span>
<span data-ttu-id="d842d-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d842d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d842d-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d842d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d842d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d842d-137">CommonParameters</span></span>
<span data-ttu-id="d842d-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d842d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d842d-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d842d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d842d-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="d842d-140">INPUTS</span></span>

### <span data-ttu-id="d842d-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d842d-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d842d-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="d842d-142">OUTPUTS</span></span>

### <span data-ttu-id="d842d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d842d-143">System.Boolean</span></span>

## <span data-ttu-id="d842d-144">Notas</span><span class="sxs-lookup"><span data-stu-id="d842d-144">NOTES</span></span>

<span data-ttu-id="d842d-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="d842d-145">ALIASES</span></span>

<span data-ttu-id="d842d-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="d842d-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d842d-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d842d-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d842d-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d842d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d842d-149">INPUTOBJECT: <IMySqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="d842d-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d842d-150">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="d842d-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d842d-151">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d842d-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d842d-152">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="d842d-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d842d-153">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="d842d-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d842d-154">`[KeyName <String>]`: o nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="d842d-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="d842d-155">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="d842d-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d842d-156">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d842d-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d842d-157">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d842d-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="d842d-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="d842d-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d842d-159">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d842d-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d842d-160">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d842d-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d842d-161">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d842d-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d842d-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d842d-162">RELATED LINKS</span></span>

