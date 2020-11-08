---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7775c4adeef0ce4b05efa2b54c6484408256f3eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124583"
---
# <span data-ttu-id="de2fb-101">Remove-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="de2fb-101">Remove-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="de2fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de2fb-102">SYNOPSIS</span></span>
<span data-ttu-id="de2fb-103">Exclui uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="de2fb-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="de2fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de2fb-104">SYNTAX</span></span>

### <span data-ttu-id="de2fb-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="de2fb-105">Delete (Default)</span></span>
```
Remove-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="de2fb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="de2fb-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="de2fb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de2fb-107">DESCRIPTION</span></span>
<span data-ttu-id="de2fb-108">Exclui uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="de2fb-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="de2fb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de2fb-109">EXAMPLES</span></span>

### <span data-ttu-id="de2fb-110">Exemplo 1: remover uma regra de firewall em um MariaDB</span><span class="sxs-lookup"><span data-stu-id="de2fb-110">Example 1: Remove a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbFirewallRule -Name frname-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

```

<span data-ttu-id="de2fb-111">Esse comando Remove uma regra de firewall em um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="de2fb-111">This command removes a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="de2fb-112">OS</span><span class="sxs-lookup"><span data-stu-id="de2fb-112">PARAMETERS</span></span>

### <span data-ttu-id="de2fb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de2fb-113">-AsJob</span></span>
<span data-ttu-id="de2fb-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="de2fb-114">Run the command as a job</span></span>

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

### <span data-ttu-id="de2fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de2fb-115">-DefaultProfile</span></span>
<span data-ttu-id="de2fb-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de2fb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de2fb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de2fb-117">-InputObject</span></span>
<span data-ttu-id="de2fb-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="de2fb-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="de2fb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="de2fb-119">-Name</span></span>
<span data-ttu-id="de2fb-120">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="de2fb-120">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="de2fb-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="de2fb-121">-NoWait</span></span>
<span data-ttu-id="de2fb-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="de2fb-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="de2fb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de2fb-123">-PassThru</span></span>
<span data-ttu-id="de2fb-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="de2fb-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="de2fb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de2fb-125">-ResourceGroupName</span></span>
<span data-ttu-id="de2fb-126">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="de2fb-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="de2fb-127">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="de2fb-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="de2fb-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="de2fb-128">-ServerName</span></span>
<span data-ttu-id="de2fb-129">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="de2fb-129">The name of the server.</span></span>

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

### <span data-ttu-id="de2fb-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de2fb-130">-SubscriptionId</span></span>
<span data-ttu-id="de2fb-131">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="de2fb-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="de2fb-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="de2fb-132">-Confirm</span></span>
<span data-ttu-id="de2fb-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de2fb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de2fb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de2fb-134">-WhatIf</span></span>
<span data-ttu-id="de2fb-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="de2fb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de2fb-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de2fb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de2fb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de2fb-137">CommonParameters</span></span>
<span data-ttu-id="de2fb-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de2fb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de2fb-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de2fb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de2fb-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de2fb-140">INPUTS</span></span>

### <span data-ttu-id="de2fb-141">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="de2fb-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="de2fb-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de2fb-142">OUTPUTS</span></span>

### <span data-ttu-id="de2fb-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de2fb-143">System.Boolean</span></span>

## <span data-ttu-id="de2fb-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de2fb-144">NOTES</span></span>

<span data-ttu-id="de2fb-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="de2fb-145">ALIASES</span></span>

<span data-ttu-id="de2fb-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="de2fb-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="de2fb-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="de2fb-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="de2fb-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="de2fb-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="de2fb-149">INPUTobject <IMariaDbIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="de2fb-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="de2fb-150">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="de2fb-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="de2fb-151">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="de2fb-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="de2fb-152">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="de2fb-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="de2fb-153">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="de2fb-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="de2fb-154">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="de2fb-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="de2fb-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="de2fb-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="de2fb-156">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="de2fb-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="de2fb-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="de2fb-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="de2fb-158">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="de2fb-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="de2fb-159">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="de2fb-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="de2fb-160">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="de2fb-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="de2fb-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de2fb-161">RELATED LINKS</span></span>

