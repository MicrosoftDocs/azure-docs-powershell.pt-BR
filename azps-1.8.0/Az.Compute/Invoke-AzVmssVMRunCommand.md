---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: 3b944b34553561f65c78f5d5581e692a4f8095c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771186"
---
# <span data-ttu-id="4c655-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="4c655-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="4c655-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c655-102">SYNOPSIS</span></span>
<span data-ttu-id="4c655-103">Comando executar na VM do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4c655-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="4c655-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c655-104">SYNTAX</span></span>

### <span data-ttu-id="4c655-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="4c655-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c655-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4c655-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c655-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4c655-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c655-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c655-108">DESCRIPTION</span></span>
<span data-ttu-id="4c655-109">Invocar um comando executar no conjunto de dimensionamento da máquina virtual VM.</span><span class="sxs-lookup"><span data-stu-id="4c655-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="4c655-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c655-110">EXAMPLES</span></span>

### <span data-ttu-id="4c655-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4c655-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="4c655-112">Invocar um comando de execução do RunPowerShellScript com a substituição do script ' sample.ps1 ' e os parâmetros na VM da ID ' 0 ' no conjunto de escala da máquina virtual de ' vmssname ' no grupo de recursos ' rgname '.</span><span class="sxs-lookup"><span data-stu-id="4c655-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="4c655-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4c655-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="4c655-114">Invocar um comando de execução do RunPowerShellScript com a substituição do script ' sample.ps1 ' e os parâmetros na VM da ID ' 0 ' no conjunto de escala da máquina virtual de ' vmssname ' no grupo de recursos ' rgname '.</span><span class="sxs-lookup"><span data-stu-id="4c655-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="4c655-115">OS</span><span class="sxs-lookup"><span data-stu-id="4c655-115">PARAMETERS</span></span>

### <span data-ttu-id="4c655-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c655-116">-AsJob</span></span>
<span data-ttu-id="4c655-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4c655-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c655-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="4c655-118">-CommandId</span></span>
<span data-ttu-id="4c655-119">A ID do comando Run.</span><span class="sxs-lookup"><span data-stu-id="4c655-119">The run command id.</span></span>

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

### <span data-ttu-id="4c655-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c655-120">-DefaultProfile</span></span>
<span data-ttu-id="4c655-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c655-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c655-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="4c655-122">-InstanceId</span></span>
<span data-ttu-id="4c655-123">A ID da instância da VM do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4c655-123">The instance ID of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="4c655-124">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c655-124">-Parameter</span></span>
<span data-ttu-id="4c655-125">Os parâmetros do comando Run.</span><span class="sxs-lookup"><span data-stu-id="4c655-125">The run command parameters.</span></span>

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

### <span data-ttu-id="4c655-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c655-126">-ResourceGroupName</span></span>
<span data-ttu-id="4c655-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4c655-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="4c655-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c655-128">-ResourceId</span></span>
<span data-ttu-id="4c655-129">A ID do recurso para a VM do conjunto de escala da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="4c655-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="4c655-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="4c655-130">-ScriptPath</span></span>
<span data-ttu-id="4c655-131">Caminho do script a ser executado.</span><span class="sxs-lookup"><span data-stu-id="4c655-131">Path of the script to be executed.</span></span>  <span data-ttu-id="4c655-132">Quando esse valor for fornecido, o script fornecido substituirá o script padrão do comando.</span><span class="sxs-lookup"><span data-stu-id="4c655-132">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="4c655-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="4c655-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="4c655-134">O objeto da máquina virtual PS da máquina virtual PS.</span><span class="sxs-lookup"><span data-stu-id="4c655-134">The PS Virtual Machine Scale Set VM Object.</span></span>

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

### <span data-ttu-id="4c655-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4c655-135">-VMScaleSetName</span></span>
<span data-ttu-id="4c655-136">O nome da VM do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4c655-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="4c655-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4c655-137">-Confirm</span></span>
<span data-ttu-id="4c655-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c655-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c655-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c655-139">-WhatIf</span></span>
<span data-ttu-id="4c655-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c655-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c655-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c655-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c655-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c655-142">CommonParameters</span></span>
<span data-ttu-id="4c655-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c655-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c655-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c655-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c655-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c655-145">INPUTS</span></span>

### <span data-ttu-id="4c655-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4c655-146">System.String</span></span>

### <span data-ttu-id="4c655-147">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="4c655-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="4c655-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c655-148">OUTPUTS</span></span>

### <span data-ttu-id="4c655-149">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="4c655-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="4c655-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c655-150">NOTES</span></span>

## <span data-ttu-id="4c655-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c655-151">RELATED LINKS</span></span>
