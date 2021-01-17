---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 474b4dc71658c1b8d79577f029d7ce0e098cca91
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429165"
---
# <span data-ttu-id="2362c-101">Remove-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2362c-101">Remove-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="2362c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2362c-102">SYNOPSIS</span></span>
<span data-ttu-id="2362c-103">Exclui a regra de rede virtual com o nome fornecido.</span><span class="sxs-lookup"><span data-stu-id="2362c-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="2362c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2362c-104">SYNTAX</span></span>

### <span data-ttu-id="2362c-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="2362c-105">Delete (Default)</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2362c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2362c-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2362c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2362c-107">DESCRIPTION</span></span>
<span data-ttu-id="2362c-108">Exclui a regra de rede virtual com o nome fornecido.</span><span class="sxs-lookup"><span data-stu-id="2362c-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="2362c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2362c-109">EXAMPLES</span></span>

### <span data-ttu-id="2362c-110">Exemplo 1: remover uma regra de rede virtual</span><span class="sxs-lookup"><span data-stu-id="2362c-110">Example 1: Remove a virtual network rule</span></span>
```powershell
PS C:\> Remove-AzMariaDbVirtualNetworkRule -Name vnet-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

```

<span data-ttu-id="2362c-111">Este comando Remove uma regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2362c-111">This command removes a virtual network rule.</span></span>

## <span data-ttu-id="2362c-112">OS</span><span class="sxs-lookup"><span data-stu-id="2362c-112">PARAMETERS</span></span>

### <span data-ttu-id="2362c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2362c-113">-AsJob</span></span>
<span data-ttu-id="2362c-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="2362c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2362c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2362c-115">-DefaultProfile</span></span>
<span data-ttu-id="2362c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2362c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2362c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2362c-117">-InputObject</span></span>
<span data-ttu-id="2362c-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2362c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2362c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2362c-119">-Name</span></span>
<span data-ttu-id="2362c-120">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2362c-120">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="2362c-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2362c-121">-NoWait</span></span>
<span data-ttu-id="2362c-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="2362c-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2362c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2362c-123">-PassThru</span></span>
<span data-ttu-id="2362c-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="2362c-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2362c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2362c-125">-ResourceGroupName</span></span>
<span data-ttu-id="2362c-126">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="2362c-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2362c-127">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="2362c-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2362c-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="2362c-128">-ServerName</span></span>
<span data-ttu-id="2362c-129">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="2362c-129">The name of the server.</span></span>

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

### <span data-ttu-id="2362c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2362c-130">-SubscriptionId</span></span>
<span data-ttu-id="2362c-131">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="2362c-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="2362c-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2362c-132">-Confirm</span></span>
<span data-ttu-id="2362c-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2362c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2362c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2362c-134">-WhatIf</span></span>
<span data-ttu-id="2362c-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2362c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2362c-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2362c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2362c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2362c-137">CommonParameters</span></span>
<span data-ttu-id="2362c-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2362c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2362c-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2362c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2362c-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2362c-140">INPUTS</span></span>

### <span data-ttu-id="2362c-141">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="2362c-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="2362c-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2362c-142">OUTPUTS</span></span>

### <span data-ttu-id="2362c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2362c-143">System.Boolean</span></span>

## <span data-ttu-id="2362c-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2362c-144">NOTES</span></span>

<span data-ttu-id="2362c-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2362c-145">ALIASES</span></span>

<span data-ttu-id="2362c-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="2362c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2362c-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="2362c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2362c-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2362c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2362c-149">INPUTobject <IMariaDbIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="2362c-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2362c-150">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="2362c-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2362c-151">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2362c-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2362c-152">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="2362c-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2362c-153">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="2362c-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2362c-154">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="2362c-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2362c-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="2362c-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="2362c-156">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="2362c-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="2362c-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="2362c-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2362c-158">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="2362c-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2362c-159">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="2362c-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="2362c-160">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2362c-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2362c-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2362c-161">RELATED LINKS</span></span>

