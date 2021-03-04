---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/remove-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 3ac6a8bf0ff61365122dce7bb537732ee187006a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892143"
---
# <span data-ttu-id="074a2-101">Remove-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="074a2-101">Remove-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="074a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="074a2-102">SYNOPSIS</span></span>
<span data-ttu-id="074a2-103">Exclui a regra de rede virtual com o nome determinado.</span><span class="sxs-lookup"><span data-stu-id="074a2-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="074a2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="074a2-104">SYNTAX</span></span>

### <span data-ttu-id="074a2-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="074a2-105">Delete (Default)</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="074a2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="074a2-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="074a2-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="074a2-107">DESCRIPTION</span></span>
<span data-ttu-id="074a2-108">Exclui a regra de rede virtual com o nome determinado.</span><span class="sxs-lookup"><span data-stu-id="074a2-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="074a2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="074a2-109">EXAMPLES</span></span>

### <span data-ttu-id="074a2-110">Exemplo 1: Remover uma regra de rede virtual</span><span class="sxs-lookup"><span data-stu-id="074a2-110">Example 1: Remove a virtual network rule</span></span>
```powershell
PS C:\> Remove-AzMariaDbVirtualNetworkRule -Name vnet-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

```

<span data-ttu-id="074a2-111">Este comando remove uma regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="074a2-111">This command removes a virtual network rule.</span></span>

## <span data-ttu-id="074a2-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="074a2-112">PARAMETERS</span></span>

### <span data-ttu-id="074a2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="074a2-113">-AsJob</span></span>
<span data-ttu-id="074a2-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="074a2-114">Run the command as a job</span></span>

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

### <span data-ttu-id="074a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="074a2-115">-DefaultProfile</span></span>
<span data-ttu-id="074a2-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="074a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="074a2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="074a2-117">-InputObject</span></span>
<span data-ttu-id="074a2-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="074a2-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="074a2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="074a2-119">-Name</span></span>
<span data-ttu-id="074a2-120">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="074a2-120">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="074a2-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="074a2-121">-NoWait</span></span>
<span data-ttu-id="074a2-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="074a2-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="074a2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="074a2-123">-PassThru</span></span>
<span data-ttu-id="074a2-124">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="074a2-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="074a2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="074a2-125">-ResourceGroupName</span></span>
<span data-ttu-id="074a2-126">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="074a2-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="074a2-127">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="074a2-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="074a2-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="074a2-128">-ServerName</span></span>
<span data-ttu-id="074a2-129">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="074a2-129">The name of the server.</span></span>

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

### <span data-ttu-id="074a2-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="074a2-130">-SubscriptionId</span></span>
<span data-ttu-id="074a2-131">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="074a2-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="074a2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="074a2-132">-Confirm</span></span>
<span data-ttu-id="074a2-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="074a2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="074a2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="074a2-134">-WhatIf</span></span>
<span data-ttu-id="074a2-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="074a2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="074a2-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="074a2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="074a2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="074a2-137">CommonParameters</span></span>
<span data-ttu-id="074a2-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="074a2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="074a2-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="074a2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="074a2-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="074a2-140">INPUTS</span></span>

### <span data-ttu-id="074a2-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="074a2-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="074a2-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="074a2-142">OUTPUTS</span></span>

### <span data-ttu-id="074a2-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="074a2-143">System.Boolean</span></span>

## <span data-ttu-id="074a2-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="074a2-144">NOTES</span></span>

<span data-ttu-id="074a2-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="074a2-145">ALIASES</span></span>

<span data-ttu-id="074a2-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="074a2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="074a2-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="074a2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="074a2-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="074a2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="074a2-149">INPUTOBJECT <IMariaDbIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="074a2-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="074a2-150">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="074a2-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="074a2-151">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="074a2-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="074a2-152">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="074a2-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="074a2-153">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="074a2-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="074a2-154">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="074a2-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="074a2-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="074a2-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="074a2-156">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="074a2-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="074a2-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="074a2-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="074a2-158">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="074a2-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="074a2-159">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="074a2-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="074a2-160">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="074a2-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="074a2-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="074a2-161">RELATED LINKS</span></span>

