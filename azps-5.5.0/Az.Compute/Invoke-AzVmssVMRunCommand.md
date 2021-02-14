---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: a63f945c5af1d5b979a0d8b70546d48233d14f00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116535"
---
# <span data-ttu-id="2ba0d-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="2ba0d-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="2ba0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ba0d-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba0d-103">Comando Executar no VM de Conjunto de Escala de Máquina Virtual.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="2ba0d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ba0d-104">SYNTAX</span></span>

### <span data-ttu-id="2ba0d-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2ba0d-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ba0d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2ba0d-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ba0d-107">Objectparameter</span><span class="sxs-lookup"><span data-stu-id="2ba0d-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ba0d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ba0d-108">DESCRIPTION</span></span>
<span data-ttu-id="2ba0d-109">Invoke a run command on the Virtual Machine Scale Set VM.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="2ba0d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2ba0d-110">EXAMPLES</span></span>

### <span data-ttu-id="2ba0d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2ba0d-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="2ba0d-112">Invocar um comando de executar do RunPowerShellScript substituindo o script "sample.ps1" e os parâmetros na ID '0' VM no conjunto de escala de máquina virtual de 'nomedovssname' no grupo de recursos 'rgname'.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="2ba0d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2ba0d-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="2ba0d-114">Invocar um comando de executar do RunPowerShellScript substituindo o script "sample.ps1" e os parâmetros na ID '0' VM no conjunto de escala de máquina virtual de 'nomedovssname' no grupo de recursos 'rgname'.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="2ba0d-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ba0d-115">PARAMETERS</span></span>

### <span data-ttu-id="2ba0d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ba0d-116">-AsJob</span></span>
<span data-ttu-id="2ba0d-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2ba0d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ba0d-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="2ba0d-118">-CommandId</span></span>
<span data-ttu-id="2ba0d-119">A ID do comando Executar.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-119">The run command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba0d-120">-DefaultProfile</span></span>
<span data-ttu-id="2ba0d-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0d-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2ba0d-122">-InstanceId</span></span>
<span data-ttu-id="2ba0d-123">A ID de instância do VM definido em escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-123">The instance ID of the virtual machine scale set VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0d-124">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ba0d-124">-Parameter</span></span>
<span data-ttu-id="2ba0d-125">Os parâmetros de comando executar.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-125">The run command parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ba0d-126">-ResourceGroupName</span></span>
<span data-ttu-id="2ba0d-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ba0d-128">-ResourceId</span></span>
<span data-ttu-id="2ba0d-129">A ID do recurso para o VM de escala de máquina virtual definido</span><span class="sxs-lookup"><span data-stu-id="2ba0d-129">The resource id for the virtual machine scale set VM</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0d-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="2ba0d-130">-ScriptPath</span></span>
<span data-ttu-id="2ba0d-131">Caminho do script a ser executado.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-131">Path of the script to be executed.</span></span>  <span data-ttu-id="2ba0d-132">Quando esse valor é dado, o script determinado substituirá o script padrão do comando.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-132">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0d-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2ba0d-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="2ba0d-134">O objeto VM de conjunto de escala de computador virtual PS.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-134">The PS Virtual Machine Scale Set VM Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0d-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2ba0d-135">-VMScaleSetName</span></span>
<span data-ttu-id="2ba0d-136">O nome do VM de escala de máquina virtual definido.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-136">The name of the virtual machine scale set VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0d-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2ba0d-137">-Confirm</span></span>
<span data-ttu-id="2ba0d-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ba0d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ba0d-139">-WhatIf</span></span>
<span data-ttu-id="2ba0d-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ba0d-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ba0d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba0d-142">CommonParameters</span></span>
<span data-ttu-id="2ba0d-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ba0d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba0d-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ba0d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba0d-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="2ba0d-145">INPUTS</span></span>

### <span data-ttu-id="2ba0d-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2ba0d-146">System.String</span></span>

### <span data-ttu-id="2ba0d-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2ba0d-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="2ba0d-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="2ba0d-148">OUTPUTS</span></span>

### <span data-ttu-id="2ba0d-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="2ba0d-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="2ba0d-150">Notas</span><span class="sxs-lookup"><span data-stu-id="2ba0d-150">NOTES</span></span>

## <span data-ttu-id="2ba0d-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ba0d-151">RELATED LINKS</span></span>
