---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: 72e7df2a9f543af6b3247e400d55ac0f9c14ce0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893199"
---
# <span data-ttu-id="404ab-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="404ab-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="404ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="404ab-102">SYNOPSIS</span></span>
<span data-ttu-id="404ab-103">A operação para remover uma identidade de máquina híbrida no Azure.</span><span class="sxs-lookup"><span data-stu-id="404ab-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="404ab-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="404ab-104">SYNTAX</span></span>

### <span data-ttu-id="404ab-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="404ab-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="404ab-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="404ab-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="404ab-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="404ab-107">DESCRIPTION</span></span>
<span data-ttu-id="404ab-108">A operação para remover uma identidade de máquina híbrida no Azure.</span><span class="sxs-lookup"><span data-stu-id="404ab-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="404ab-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="404ab-109">EXAMPLES</span></span>

### <span data-ttu-id="404ab-110">Exemplo 1: Remover um computador conectado</span><span class="sxs-lookup"><span data-stu-id="404ab-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="404ab-111">Exclui o computador conectado.</span><span class="sxs-lookup"><span data-stu-id="404ab-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="404ab-112">Exemplo 2: Remover máquinas conectadas por meio do pipeline</span><span class="sxs-lookup"><span data-stu-id="404ab-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="404ab-113">Remove todos os máquinas do `contoso-connected-machines` grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="404ab-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="404ab-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="404ab-114">PARAMETERS</span></span>

### <span data-ttu-id="404ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="404ab-115">-DefaultProfile</span></span>
<span data-ttu-id="404ab-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="404ab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="404ab-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="404ab-117">-InputObject</span></span>
<span data-ttu-id="404ab-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="404ab-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="404ab-119">-Name</span><span class="sxs-lookup"><span data-stu-id="404ab-119">-Name</span></span>
<span data-ttu-id="404ab-120">O nome da máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="404ab-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="404ab-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="404ab-121">-PassThru</span></span>
<span data-ttu-id="404ab-122">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="404ab-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="404ab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="404ab-123">-ResourceGroupName</span></span>
<span data-ttu-id="404ab-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="404ab-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="404ab-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="404ab-125">-SubscriptionId</span></span>
<span data-ttu-id="404ab-126">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="404ab-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="404ab-127">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="404ab-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="404ab-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="404ab-128">-Confirm</span></span>
<span data-ttu-id="404ab-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="404ab-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="404ab-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="404ab-130">-WhatIf</span></span>
<span data-ttu-id="404ab-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="404ab-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="404ab-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="404ab-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="404ab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="404ab-133">CommonParameters</span></span>
<span data-ttu-id="404ab-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="404ab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="404ab-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="404ab-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="404ab-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="404ab-136">INPUTS</span></span>

### <span data-ttu-id="404ab-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="404ab-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="404ab-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="404ab-138">OUTPUTS</span></span>

### <span data-ttu-id="404ab-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="404ab-139">System.Boolean</span></span>

## <span data-ttu-id="404ab-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="404ab-140">NOTES</span></span>

<span data-ttu-id="404ab-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="404ab-141">ALIASES</span></span>

<span data-ttu-id="404ab-142">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="404ab-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="404ab-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="404ab-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="404ab-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="404ab-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="404ab-145">INPUTOBJECT <IConnectedMachineIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="404ab-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="404ab-146">`[ExtensionName <String>]`: O nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="404ab-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="404ab-147">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="404ab-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="404ab-148">`[Name <String>]`: O nome da máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="404ab-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="404ab-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="404ab-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="404ab-150">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="404ab-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="404ab-151">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="404ab-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="404ab-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="404ab-152">RELATED LINKS</span></span>

