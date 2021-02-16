---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7775c4adeef0ce4b05efa2b54c6484408256f3eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117568"
---
# <span data-ttu-id="bbfe3-101">Remove-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bbfe3-101">Remove-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="bbfe3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bbfe3-102">SYNOPSIS</span></span>
<span data-ttu-id="bbfe3-103">Exclui uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="bbfe3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbfe3-104">SYNTAX</span></span>

### <span data-ttu-id="bbfe3-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bbfe3-105">Delete (Default)</span></span>
```
Remove-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="bbfe3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bbfe3-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bbfe3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbfe3-107">DESCRIPTION</span></span>
<span data-ttu-id="bbfe3-108">Exclui uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="bbfe3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bbfe3-109">EXAMPLES</span></span>

### <span data-ttu-id="bbfe3-110">Exemplo 1: Remover uma regra de firewall sob um MariaDB</span><span class="sxs-lookup"><span data-stu-id="bbfe3-110">Example 1: Remove a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbFirewallRule -Name frname-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

```

<span data-ttu-id="bbfe3-111">Esse comando remove uma regra de firewall sob um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-111">This command removes a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="bbfe3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbfe3-112">PARAMETERS</span></span>

### <span data-ttu-id="bbfe3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbfe3-113">-AsJob</span></span>
<span data-ttu-id="bbfe3-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="bbfe3-114">Run the command as a job</span></span>

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

### <span data-ttu-id="bbfe3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbfe3-115">-DefaultProfile</span></span>
<span data-ttu-id="bbfe3-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbfe3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbfe3-117">-InputObject</span></span>
<span data-ttu-id="bbfe3-118">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbfe3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbfe3-119">-Name</span></span>
<span data-ttu-id="bbfe3-120">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-120">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="bbfe3-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bbfe3-121">-NoWait</span></span>
<span data-ttu-id="bbfe3-122">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="bbfe3-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bbfe3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbfe3-123">-PassThru</span></span>
<span data-ttu-id="bbfe3-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="bbfe3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bbfe3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbfe3-125">-ResourceGroupName</span></span>
<span data-ttu-id="bbfe3-126">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="bbfe3-127">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="bbfe3-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bbfe3-128">-ServerName</span></span>
<span data-ttu-id="bbfe3-129">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-129">The name of the server.</span></span>

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

### <span data-ttu-id="bbfe3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bbfe3-130">-SubscriptionId</span></span>
<span data-ttu-id="bbfe3-131">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="bbfe3-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bbfe3-132">-Confirm</span></span>
<span data-ttu-id="bbfe3-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbfe3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbfe3-134">-WhatIf</span></span>
<span data-ttu-id="bbfe3-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbfe3-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbfe3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbfe3-137">CommonParameters</span></span>
<span data-ttu-id="bbfe3-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbfe3-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbfe3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbfe3-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="bbfe3-140">INPUTS</span></span>

### <span data-ttu-id="bbfe3-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="bbfe3-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="bbfe3-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="bbfe3-142">OUTPUTS</span></span>

### <span data-ttu-id="bbfe3-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bbfe3-143">System.Boolean</span></span>

## <span data-ttu-id="bbfe3-144">Notas</span><span class="sxs-lookup"><span data-stu-id="bbfe3-144">NOTES</span></span>

<span data-ttu-id="bbfe3-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="bbfe3-145">ALIASES</span></span>

<span data-ttu-id="bbfe3-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="bbfe3-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bbfe3-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bbfe3-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bbfe3-149">INPUTOBJECT: <IMariaDbIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="bbfe3-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bbfe3-150">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="bbfe3-151">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="bbfe3-152">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="bbfe3-153">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="bbfe3-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bbfe3-154">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="bbfe3-155">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="bbfe3-156">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="bbfe3-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="bbfe3-158">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="bbfe3-159">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="bbfe3-160">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="bbfe3-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="bbfe3-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbfe3-161">RELATED LINKS</span></span>

