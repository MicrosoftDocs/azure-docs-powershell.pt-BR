---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434140"
---
# <span data-ttu-id="26533-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="26533-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="26533-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26533-102">SYNOPSIS</span></span>
<span data-ttu-id="26533-103">A operação para excluir a extensão.</span><span class="sxs-lookup"><span data-stu-id="26533-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="26533-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26533-104">SYNTAX</span></span>

### <span data-ttu-id="26533-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="26533-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="26533-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="26533-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="26533-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26533-107">DESCRIPTION</span></span>
<span data-ttu-id="26533-108">A operação para excluir a extensão.</span><span class="sxs-lookup"><span data-stu-id="26533-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="26533-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26533-109">EXAMPLES</span></span>

### <span data-ttu-id="26533-110">Exemplo 1: remover uma extensão de computador.</span><span class="sxs-lookup"><span data-stu-id="26533-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="26533-111">Exclui a extensão na máquina.</span><span class="sxs-lookup"><span data-stu-id="26533-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="26533-112">Exemplo 2: remover extensão pelo pipeline</span><span class="sxs-lookup"><span data-stu-id="26533-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="26533-113">Remove todas as extensões no computador especificado.</span><span class="sxs-lookup"><span data-stu-id="26533-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="26533-114">OS</span><span class="sxs-lookup"><span data-stu-id="26533-114">PARAMETERS</span></span>

### <span data-ttu-id="26533-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26533-115">-AsJob</span></span>
<span data-ttu-id="26533-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="26533-116">Run the command as a job</span></span>

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

### <span data-ttu-id="26533-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26533-117">-DefaultProfile</span></span>
<span data-ttu-id="26533-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="26533-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26533-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26533-119">-InputObject</span></span>
<span data-ttu-id="26533-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="26533-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="26533-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="26533-121">-MachineName</span></span>
<span data-ttu-id="26533-122">O nome da máquina na qual a extensão deve ser excluída.</span><span class="sxs-lookup"><span data-stu-id="26533-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="26533-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="26533-123">-Name</span></span>
<span data-ttu-id="26533-124">O nome da extensão da máquina.</span><span class="sxs-lookup"><span data-stu-id="26533-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="26533-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="26533-125">-NoWait</span></span>
<span data-ttu-id="26533-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="26533-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="26533-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26533-127">-PassThru</span></span>
<span data-ttu-id="26533-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="26533-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="26533-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26533-129">-ResourceGroupName</span></span>
<span data-ttu-id="26533-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="26533-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="26533-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26533-131">-SubscriptionId</span></span>
<span data-ttu-id="26533-132">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="26533-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="26533-133">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="26533-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="26533-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="26533-134">-Confirm</span></span>
<span data-ttu-id="26533-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26533-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26533-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26533-136">-WhatIf</span></span>
<span data-ttu-id="26533-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="26533-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26533-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="26533-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26533-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26533-139">CommonParameters</span></span>
<span data-ttu-id="26533-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26533-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26533-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26533-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26533-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26533-142">INPUTS</span></span>

### <span data-ttu-id="26533-143">Microsoft. Azure. PowerShell. cmdlets. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="26533-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="26533-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26533-144">OUTPUTS</span></span>

### <span data-ttu-id="26533-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26533-145">System.Boolean</span></span>

## <span data-ttu-id="26533-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26533-146">NOTES</span></span>

<span data-ttu-id="26533-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="26533-147">ALIASES</span></span>

<span data-ttu-id="26533-148">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="26533-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="26533-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="26533-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="26533-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="26533-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="26533-151">INPUTobject <IConnectedMachineIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="26533-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="26533-152">`[ExtensionName <String>]`: O nome da extensão da máquina.</span><span class="sxs-lookup"><span data-stu-id="26533-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="26533-153">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="26533-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="26533-154">`[Name <String>]`: O nome da máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="26533-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="26533-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="26533-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="26533-156">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="26533-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="26533-157">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="26533-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="26533-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26533-158">RELATED LINKS</span></span>

