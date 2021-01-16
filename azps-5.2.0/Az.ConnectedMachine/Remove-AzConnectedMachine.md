---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257078"
---
# <span data-ttu-id="a8ee4-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="a8ee4-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="a8ee4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ee4-103">A operação para remover uma identidade de computador híbrido no Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="a8ee4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8ee4-104">SYNTAX</span></span>

### <span data-ttu-id="a8ee4-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="a8ee4-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a8ee4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a8ee4-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a8ee4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a8ee4-107">DESCRIPTION</span></span>
<span data-ttu-id="a8ee4-108">A operação para remover uma identidade de computador híbrido no Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="a8ee4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8ee4-109">EXAMPLES</span></span>

### <span data-ttu-id="a8ee4-110">Exemplo 1: remover uma máquina conectada</span><span class="sxs-lookup"><span data-stu-id="a8ee4-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="a8ee4-111">Exclui a máquina conectada.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="a8ee4-112">Exemplo 2: remover máquinas conectadas via pipeline</span><span class="sxs-lookup"><span data-stu-id="a8ee4-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="a8ee4-113">Remove todas as máquinas do `contoso-connected-machines` grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="a8ee4-114">OS</span><span class="sxs-lookup"><span data-stu-id="a8ee4-114">PARAMETERS</span></span>

### <span data-ttu-id="a8ee4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ee4-115">-DefaultProfile</span></span>
<span data-ttu-id="a8ee4-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8ee4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8ee4-117">-InputObject</span></span>
<span data-ttu-id="a8ee4-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a8ee4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8ee4-119">-Name</span></span>
<span data-ttu-id="a8ee4-120">O nome da máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="a8ee4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8ee4-121">-PassThru</span></span>
<span data-ttu-id="a8ee4-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="a8ee4-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a8ee4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8ee4-123">-ResourceGroupName</span></span>
<span data-ttu-id="a8ee4-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a8ee4-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8ee4-125">-SubscriptionId</span></span>
<span data-ttu-id="a8ee4-126">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a8ee4-127">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a8ee4-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a8ee4-128">-Confirm</span></span>
<span data-ttu-id="a8ee4-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8ee4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ee4-130">-WhatIf</span></span>
<span data-ttu-id="a8ee4-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8ee4-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8ee4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ee4-133">CommonParameters</span></span>
<span data-ttu-id="a8ee4-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ee4-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8ee4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ee4-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a8ee4-136">INPUTS</span></span>

### <span data-ttu-id="a8ee4-137">Microsoft. Azure. PowerShell. cmdlets. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="a8ee4-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="a8ee4-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a8ee4-138">OUTPUTS</span></span>

### <span data-ttu-id="a8ee4-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8ee4-139">System.Boolean</span></span>

## <span data-ttu-id="a8ee4-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a8ee4-140">NOTES</span></span>

<span data-ttu-id="a8ee4-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a8ee4-141">ALIASES</span></span>

<span data-ttu-id="a8ee4-142">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="a8ee4-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a8ee4-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a8ee4-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a8ee4-145">INPUTobject <IConnectedMachineIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="a8ee4-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a8ee4-146">`[ExtensionName <String>]`: O nome da extensão da máquina.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="a8ee4-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a8ee4-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a8ee4-148">`[Name <String>]`: O nome da máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="a8ee4-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a8ee4-150">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a8ee4-151">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a8ee4-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8ee4-152">RELATED LINKS</span></span>

