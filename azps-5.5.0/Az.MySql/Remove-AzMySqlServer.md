---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
ms.openlocfilehash: 9e113eddbbc05dc55da75cccd7650cdf3adfdc74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111727"
---
# <span data-ttu-id="13059-101">Remove-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="13059-101">Remove-AzMySqlServer</span></span>

## <span data-ttu-id="13059-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13059-102">SYNOPSIS</span></span>
<span data-ttu-id="13059-103">Exclui um servidor.</span><span class="sxs-lookup"><span data-stu-id="13059-103">Deletes a server.</span></span>

## <span data-ttu-id="13059-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13059-104">SYNTAX</span></span>

### <span data-ttu-id="13059-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="13059-105">Delete (Default)</span></span>
```
Remove-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="13059-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="13059-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="13059-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="13059-107">DESCRIPTION</span></span>
<span data-ttu-id="13059-108">Exclui um servidor.</span><span class="sxs-lookup"><span data-stu-id="13059-108">Deletes a server.</span></span>

## <span data-ttu-id="13059-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13059-109">EXAMPLES</span></span>

### <span data-ttu-id="13059-110">Exemplo 1: Remover servidor MySql por resourceGroup e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="13059-110">Example 1: Remove MySql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="13059-111">Este cmdlet remove o servidor MySql por resourceGroup e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="13059-111">This cmdlet removes MySql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="13059-112">Exemplo 2: Remover servidor MySql por identidade</span><span class="sxs-lookup"><span data-stu-id="13059-112">Example 2: Remove MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Remove-AzMySqlServer -InputObject $ID
 
```

<span data-ttu-id="13059-113">Esses cmdlets removem o servidor MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="13059-113">These cmdlets remove MySql server by identity.</span></span>

## <span data-ttu-id="13059-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13059-114">PARAMETERS</span></span>

### <span data-ttu-id="13059-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13059-115">-AsJob</span></span>
<span data-ttu-id="13059-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="13059-116">Run the command as a job</span></span>

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

### <span data-ttu-id="13059-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13059-117">-DefaultProfile</span></span>
<span data-ttu-id="13059-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13059-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13059-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13059-119">-InputObject</span></span>
<span data-ttu-id="13059-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="13059-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13059-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="13059-121">-Name</span></span>
<span data-ttu-id="13059-122">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="13059-122">The name of the server.</span></span>

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

### <span data-ttu-id="13059-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="13059-123">-NoWait</span></span>
<span data-ttu-id="13059-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="13059-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="13059-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13059-125">-PassThru</span></span>
<span data-ttu-id="13059-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="13059-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="13059-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13059-127">-ResourceGroupName</span></span>
<span data-ttu-id="13059-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="13059-128">The name of the resource group.</span></span>
<span data-ttu-id="13059-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="13059-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="13059-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13059-130">-SubscriptionId</span></span>
<span data-ttu-id="13059-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="13059-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="13059-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="13059-132">-Confirm</span></span>
<span data-ttu-id="13059-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13059-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13059-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13059-134">-WhatIf</span></span>
<span data-ttu-id="13059-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="13059-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13059-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="13059-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13059-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13059-137">CommonParameters</span></span>
<span data-ttu-id="13059-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13059-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13059-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13059-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13059-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="13059-140">INPUTS</span></span>

### <span data-ttu-id="13059-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="13059-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="13059-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="13059-142">OUTPUTS</span></span>

### <span data-ttu-id="13059-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="13059-143">System.Boolean</span></span>

## <span data-ttu-id="13059-144">Notas</span><span class="sxs-lookup"><span data-stu-id="13059-144">NOTES</span></span>

<span data-ttu-id="13059-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="13059-145">ALIASES</span></span>

<span data-ttu-id="13059-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="13059-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="13059-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="13059-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="13059-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="13059-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="13059-149">INPUTOBJECT: <IMySqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="13059-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="13059-150">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="13059-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="13059-151">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="13059-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="13059-152">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="13059-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="13059-153">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="13059-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="13059-154">`[KeyName <String>]`: o nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="13059-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="13059-155">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="13059-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="13059-156">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="13059-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="13059-157">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="13059-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="13059-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="13059-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="13059-159">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="13059-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="13059-160">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="13059-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="13059-161">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="13059-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="13059-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13059-162">RELATED LINKS</span></span>

