---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127058"
---
# <span data-ttu-id="7974e-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="7974e-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="7974e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7974e-102">SYNOPSIS</span></span>
<span data-ttu-id="7974e-103">A operação para excluir a extensão.</span><span class="sxs-lookup"><span data-stu-id="7974e-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="7974e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7974e-104">SYNTAX</span></span>

### <span data-ttu-id="7974e-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7974e-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7974e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7974e-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7974e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7974e-107">DESCRIPTION</span></span>
<span data-ttu-id="7974e-108">A operação para excluir a extensão.</span><span class="sxs-lookup"><span data-stu-id="7974e-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="7974e-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7974e-109">EXAMPLES</span></span>

### <span data-ttu-id="7974e-110">Exemplo 1: Remover uma extensão de máquina.</span><span class="sxs-lookup"><span data-stu-id="7974e-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="7974e-111">Exclui a extensão no computador.</span><span class="sxs-lookup"><span data-stu-id="7974e-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="7974e-112">Exemplo 2: Remover extensão por meio do pipeline</span><span class="sxs-lookup"><span data-stu-id="7974e-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="7974e-113">Remove todas as extensões do computador especificado.</span><span class="sxs-lookup"><span data-stu-id="7974e-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="7974e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7974e-114">PARAMETERS</span></span>

### <span data-ttu-id="7974e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7974e-115">-AsJob</span></span>
<span data-ttu-id="7974e-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="7974e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7974e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7974e-117">-DefaultProfile</span></span>
<span data-ttu-id="7974e-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7974e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7974e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7974e-119">-InputObject</span></span>
<span data-ttu-id="7974e-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="7974e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7974e-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="7974e-121">-MachineName</span></span>
<span data-ttu-id="7974e-122">O nome da máquina onde a extensão deve ser excluída.</span><span class="sxs-lookup"><span data-stu-id="7974e-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="7974e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="7974e-123">-Name</span></span>
<span data-ttu-id="7974e-124">O nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="7974e-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="7974e-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7974e-125">-NoWait</span></span>
<span data-ttu-id="7974e-126">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="7974e-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7974e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7974e-127">-PassThru</span></span>
<span data-ttu-id="7974e-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="7974e-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7974e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7974e-129">-ResourceGroupName</span></span>
<span data-ttu-id="7974e-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7974e-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="7974e-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7974e-131">-SubscriptionId</span></span>
<span data-ttu-id="7974e-132">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7974e-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7974e-133">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7974e-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7974e-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7974e-134">-Confirm</span></span>
<span data-ttu-id="7974e-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7974e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7974e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7974e-136">-WhatIf</span></span>
<span data-ttu-id="7974e-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7974e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7974e-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7974e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7974e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7974e-139">CommonParameters</span></span>
<span data-ttu-id="7974e-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7974e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7974e-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7974e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7974e-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="7974e-142">INPUTS</span></span>

### <span data-ttu-id="7974e-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="7974e-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="7974e-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="7974e-144">OUTPUTS</span></span>

### <span data-ttu-id="7974e-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7974e-145">System.Boolean</span></span>

## <span data-ttu-id="7974e-146">Notas</span><span class="sxs-lookup"><span data-stu-id="7974e-146">NOTES</span></span>

<span data-ttu-id="7974e-147">Aliases</span><span class="sxs-lookup"><span data-stu-id="7974e-147">ALIASES</span></span>

<span data-ttu-id="7974e-148">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="7974e-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7974e-149">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="7974e-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7974e-150">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7974e-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7974e-151">INPUTOBJECT: <IConnectedMachineIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="7974e-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7974e-152">`[ExtensionName <String>]`: o nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="7974e-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="7974e-153">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="7974e-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7974e-154">`[Name <String>]`: o nome da máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="7974e-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="7974e-155">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7974e-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="7974e-156">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7974e-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7974e-157">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7974e-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7974e-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7974e-158">RELATED LINKS</span></span>

