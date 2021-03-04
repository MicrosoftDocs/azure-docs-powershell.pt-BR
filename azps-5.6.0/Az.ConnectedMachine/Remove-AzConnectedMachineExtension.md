---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: 777c02f6588d7c1fdb1a1d6e9e9c004f51694293
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893198"
---
# <span data-ttu-id="2d904-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="2d904-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="2d904-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d904-102">SYNOPSIS</span></span>
<span data-ttu-id="2d904-103">A operação para excluir a extensão.</span><span class="sxs-lookup"><span data-stu-id="2d904-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="2d904-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2d904-104">SYNTAX</span></span>

### <span data-ttu-id="2d904-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2d904-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2d904-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2d904-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2d904-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2d904-107">DESCRIPTION</span></span>
<span data-ttu-id="2d904-108">A operação para excluir a extensão.</span><span class="sxs-lookup"><span data-stu-id="2d904-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="2d904-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d904-109">EXAMPLES</span></span>

### <span data-ttu-id="2d904-110">Exemplo 1: Remover uma extensão de máquina.</span><span class="sxs-lookup"><span data-stu-id="2d904-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="2d904-111">Exclui a extensão no computador.</span><span class="sxs-lookup"><span data-stu-id="2d904-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="2d904-112">Exemplo 2: Remover extensão por meio do pipeline</span><span class="sxs-lookup"><span data-stu-id="2d904-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="2d904-113">Remove todas as extensões no computador especificado.</span><span class="sxs-lookup"><span data-stu-id="2d904-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="2d904-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2d904-114">PARAMETERS</span></span>

### <span data-ttu-id="2d904-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d904-115">-AsJob</span></span>
<span data-ttu-id="2d904-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="2d904-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2d904-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d904-117">-DefaultProfile</span></span>
<span data-ttu-id="2d904-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d904-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d904-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d904-119">-InputObject</span></span>
<span data-ttu-id="2d904-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2d904-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d904-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="2d904-121">-MachineName</span></span>
<span data-ttu-id="2d904-122">O nome do computador onde a extensão deve ser excluída.</span><span class="sxs-lookup"><span data-stu-id="2d904-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="2d904-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2d904-123">-Name</span></span>
<span data-ttu-id="2d904-124">O nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="2d904-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="2d904-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2d904-125">-NoWait</span></span>
<span data-ttu-id="2d904-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="2d904-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2d904-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d904-127">-PassThru</span></span>
<span data-ttu-id="2d904-128">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="2d904-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2d904-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d904-129">-ResourceGroupName</span></span>
<span data-ttu-id="2d904-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2d904-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="2d904-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d904-131">-SubscriptionId</span></span>
<span data-ttu-id="2d904-132">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2d904-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2d904-133">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2d904-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2d904-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d904-134">-Confirm</span></span>
<span data-ttu-id="2d904-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d904-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d904-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d904-136">-WhatIf</span></span>
<span data-ttu-id="2d904-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d904-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d904-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d904-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d904-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d904-139">CommonParameters</span></span>
<span data-ttu-id="2d904-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d904-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d904-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d904-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d904-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d904-142">INPUTS</span></span>

### <span data-ttu-id="2d904-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="2d904-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="2d904-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2d904-144">OUTPUTS</span></span>

### <span data-ttu-id="2d904-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2d904-145">System.Boolean</span></span>

## <span data-ttu-id="2d904-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="2d904-146">NOTES</span></span>

<span data-ttu-id="2d904-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2d904-147">ALIASES</span></span>

<span data-ttu-id="2d904-148">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="2d904-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2d904-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="2d904-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2d904-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2d904-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2d904-151">INPUTOBJECT <IConnectedMachineIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="2d904-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2d904-152">`[ExtensionName <String>]`: O nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="2d904-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="2d904-153">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="2d904-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2d904-154">`[Name <String>]`: O nome da máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="2d904-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="2d904-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2d904-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2d904-156">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2d904-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2d904-157">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2d904-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2d904-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d904-158">RELATED LINKS</span></span>

