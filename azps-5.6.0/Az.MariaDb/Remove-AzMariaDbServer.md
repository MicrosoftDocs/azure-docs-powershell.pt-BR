---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/remove-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
ms.openlocfilehash: e4ea7cf3b8f85b018ec087122bda8dcfeec066d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892145"
---
# <span data-ttu-id="66407-101">Remove-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="66407-101">Remove-AzMariaDbServer</span></span>

## <span data-ttu-id="66407-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66407-102">SYNOPSIS</span></span>
<span data-ttu-id="66407-103">Exclui um servidor.</span><span class="sxs-lookup"><span data-stu-id="66407-103">Deletes a server.</span></span>

## <span data-ttu-id="66407-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="66407-104">SYNTAX</span></span>

### <span data-ttu-id="66407-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="66407-105">Delete (Default)</span></span>
```
Remove-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="66407-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="66407-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="66407-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="66407-107">DESCRIPTION</span></span>
<span data-ttu-id="66407-108">Exclui um servidor.</span><span class="sxs-lookup"><span data-stu-id="66407-108">Deletes a server.</span></span>

## <span data-ttu-id="66407-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66407-109">EXAMPLES</span></span>

### <span data-ttu-id="66407-110">Exemplo 1: Remover um MariaDB</span><span class="sxs-lookup"><span data-stu-id="66407-110">Example 1: Remove a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbServer -Name mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="66407-111">Este comando remove um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="66407-111">This command removes a MariaDB.</span></span>

### <span data-ttu-id="66407-112">Exemplo 2: Remover um MariaDB</span><span class="sxs-lookup"><span data-stu-id="66407-112">Example 2: Remove a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-bc-t01 -ResourceGroupName mariadb-test-qu5ov0 | Remove-AzMariaDbServer

```

<span data-ttu-id="66407-113">Este comando remove um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="66407-113">This command removes a MariaDB.</span></span>

## <span data-ttu-id="66407-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="66407-114">PARAMETERS</span></span>

### <span data-ttu-id="66407-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66407-115">-AsJob</span></span>
<span data-ttu-id="66407-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="66407-116">Run the command as a job</span></span>

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

### <span data-ttu-id="66407-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66407-117">-DefaultProfile</span></span>
<span data-ttu-id="66407-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66407-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66407-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66407-119">-InputObject</span></span>
<span data-ttu-id="66407-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="66407-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="66407-121">-Name</span><span class="sxs-lookup"><span data-stu-id="66407-121">-Name</span></span>
<span data-ttu-id="66407-122">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="66407-122">The name of the server.</span></span>

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

### <span data-ttu-id="66407-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="66407-123">-NoWait</span></span>
<span data-ttu-id="66407-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="66407-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="66407-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66407-125">-PassThru</span></span>
<span data-ttu-id="66407-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="66407-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="66407-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66407-127">-ResourceGroupName</span></span>
<span data-ttu-id="66407-128">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="66407-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="66407-129">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="66407-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="66407-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66407-130">-SubscriptionId</span></span>
<span data-ttu-id="66407-131">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="66407-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="66407-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66407-132">-Confirm</span></span>
<span data-ttu-id="66407-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66407-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66407-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66407-134">-WhatIf</span></span>
<span data-ttu-id="66407-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="66407-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66407-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66407-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66407-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66407-137">CommonParameters</span></span>
<span data-ttu-id="66407-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66407-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66407-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66407-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66407-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66407-140">INPUTS</span></span>

### <span data-ttu-id="66407-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="66407-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="66407-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="66407-142">OUTPUTS</span></span>

### <span data-ttu-id="66407-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66407-143">System.Boolean</span></span>

## <span data-ttu-id="66407-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="66407-144">NOTES</span></span>

<span data-ttu-id="66407-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="66407-145">ALIASES</span></span>

<span data-ttu-id="66407-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="66407-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="66407-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="66407-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="66407-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="66407-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="66407-149">INPUTOBJECT <IMariaDbIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="66407-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="66407-150">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="66407-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="66407-151">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="66407-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="66407-152">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="66407-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="66407-153">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="66407-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="66407-154">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="66407-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="66407-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="66407-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="66407-156">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="66407-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="66407-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="66407-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="66407-158">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="66407-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="66407-159">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="66407-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="66407-160">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="66407-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="66407-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66407-161">RELATED LINKS</span></span>

