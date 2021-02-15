---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
ms.openlocfilehash: 481761efe01646a10118d8ebfd645375caafbfef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114227"
---
# <span data-ttu-id="c4ac8-101">Remove-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c4ac8-101">Remove-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="c4ac8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4ac8-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ac8-103">Exclui uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="c4ac8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4ac8-104">SYNTAX</span></span>

### <span data-ttu-id="c4ac8-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c4ac8-105">Delete (Default)</span></span>
```
Remove-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c4ac8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c4ac8-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c4ac8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4ac8-107">DESCRIPTION</span></span>
<span data-ttu-id="c4ac8-108">Exclui uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="c4ac8-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c4ac8-109">EXAMPLES</span></span>

### <span data-ttu-id="c4ac8-110">Exemplo 1: Remover Regra de Firewall MySql por nome</span><span class="sxs-lookup"><span data-stu-id="c4ac8-110">Example 1: Remove MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

```

<span data-ttu-id="c4ac8-111">Este cmdlet remove MySql Firewall Rule por nome.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-111">This cmdlet removes MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="c4ac8-112">Exemplo 2: Remover a Regra de Firewall MySql por identidade</span><span class="sxs-lookup"><span data-stu-id="c4ac8-112">Example 2: Remove MySql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Remove-AzMySqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="c4ac8-113">Esses cmdlets removem a Regra de Firewall MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-113">These cmdlets remove MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="c4ac8-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4ac8-114">PARAMETERS</span></span>

### <span data-ttu-id="c4ac8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4ac8-115">-AsJob</span></span>
<span data-ttu-id="c4ac8-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="c4ac8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c4ac8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ac8-117">-DefaultProfile</span></span>
<span data-ttu-id="c4ac8-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4ac8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4ac8-119">-InputObject</span></span>
<span data-ttu-id="c4ac8-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c4ac8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4ac8-121">-Name</span></span>
<span data-ttu-id="c4ac8-122">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-122">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ac8-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c4ac8-123">-NoWait</span></span>
<span data-ttu-id="c4ac8-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="c4ac8-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c4ac8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4ac8-125">-PassThru</span></span>
<span data-ttu-id="c4ac8-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="c4ac8-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c4ac8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ac8-127">-ResourceGroupName</span></span>
<span data-ttu-id="c4ac8-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-128">The name of the resource group.</span></span>
<span data-ttu-id="c4ac8-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c4ac8-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c4ac8-130">-ServerName</span></span>
<span data-ttu-id="c4ac8-131">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-131">The name of the server.</span></span>

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

### <span data-ttu-id="c4ac8-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4ac8-132">-SubscriptionId</span></span>
<span data-ttu-id="c4ac8-133">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c4ac8-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c4ac8-134">-Confirm</span></span>
<span data-ttu-id="c4ac8-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4ac8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4ac8-136">-WhatIf</span></span>
<span data-ttu-id="c4ac8-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4ac8-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4ac8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ac8-139">CommonParameters</span></span>
<span data-ttu-id="c4ac8-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ac8-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4ac8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ac8-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="c4ac8-142">INPUTS</span></span>

### <span data-ttu-id="c4ac8-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="c4ac8-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="c4ac8-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="c4ac8-144">OUTPUTS</span></span>

### <span data-ttu-id="c4ac8-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c4ac8-145">System.Boolean</span></span>

## <span data-ttu-id="c4ac8-146">Notas</span><span class="sxs-lookup"><span data-stu-id="c4ac8-146">NOTES</span></span>

<span data-ttu-id="c4ac8-147">Aliases</span><span class="sxs-lookup"><span data-stu-id="c4ac8-147">ALIASES</span></span>

<span data-ttu-id="c4ac8-148">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="c4ac8-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c4ac8-149">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4ac8-150">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c4ac8-151">INPUTOBJECT: <IMySqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="c4ac8-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4ac8-152">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c4ac8-153">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c4ac8-154">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c4ac8-155">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="c4ac8-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4ac8-156">`[KeyName <String>]`: o nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="c4ac8-157">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c4ac8-158">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c4ac8-159">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="c4ac8-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c4ac8-161">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c4ac8-162">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c4ac8-163">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c4ac8-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c4ac8-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4ac8-164">RELATED LINKS</span></span>

