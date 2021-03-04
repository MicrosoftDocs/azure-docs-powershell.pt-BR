---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 8eaf939839a668ea817d8f3529fced76ef71d22e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892224"
---
# <span data-ttu-id="6c488-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="6c488-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="6c488-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c488-102">SYNOPSIS</span></span>
<span data-ttu-id="6c488-103">Execute um comando na VM.</span><span class="sxs-lookup"><span data-stu-id="6c488-103">Run a command on the VM.</span></span>

## <span data-ttu-id="6c488-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6c488-104">SYNTAX</span></span>

### <span data-ttu-id="6c488-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6c488-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c488-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6c488-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c488-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="6c488-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c488-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6c488-108">DESCRIPTION</span></span>
<span data-ttu-id="6c488-109">Invocar um comando run na VM.</span><span class="sxs-lookup"><span data-stu-id="6c488-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="6c488-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c488-110">EXAMPLES</span></span>

### <span data-ttu-id="6c488-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6c488-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="6c488-112">Invoque um comando run de RunPowerShellScript substituindo o script 'sample.ps1' e os parâmetros na VM de 'vmname' no grupo de recursos 'rgname'.</span><span class="sxs-lookup"><span data-stu-id="6c488-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="6c488-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6c488-113">PARAMETERS</span></span>

### <span data-ttu-id="6c488-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c488-114">-AsJob</span></span>
<span data-ttu-id="6c488-115">Execute o cmdlet em segundo plano e retorne um objeto de trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="6c488-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="6c488-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="6c488-116">-CommandId</span></span>
<span data-ttu-id="6c488-117">A ID do comando run.</span><span class="sxs-lookup"><span data-stu-id="6c488-117">The run command ID.</span></span>

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

### <span data-ttu-id="6c488-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c488-118">-DefaultProfile</span></span>
<span data-ttu-id="6c488-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6c488-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c488-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="6c488-120">-Parameter</span></span>
<span data-ttu-id="6c488-121">Os parâmetros de comando executar.</span><span class="sxs-lookup"><span data-stu-id="6c488-121">The run command parameters.</span></span>

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

### <span data-ttu-id="6c488-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c488-122">-ResourceGroupName</span></span>
<span data-ttu-id="6c488-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6c488-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="6c488-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c488-124">-ResourceId</span></span>
<span data-ttu-id="6c488-125">A ID do recurso para a VM.</span><span class="sxs-lookup"><span data-stu-id="6c488-125">The resource ID for the VM.</span></span>

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

### <span data-ttu-id="6c488-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="6c488-126">-ScriptPath</span></span>
<span data-ttu-id="6c488-127">Caminho do script a ser executado.</span><span class="sxs-lookup"><span data-stu-id="6c488-127">Path of the script to be executed.</span></span>  <span data-ttu-id="6c488-128">Quando esse valor é dado, o script dado substituirá o script padrão do comando.</span><span class="sxs-lookup"><span data-stu-id="6c488-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="6c488-129">-VM</span><span class="sxs-lookup"><span data-stu-id="6c488-129">-VM</span></span>
<span data-ttu-id="6c488-130">O objeto da máquina virtual PS.</span><span class="sxs-lookup"><span data-stu-id="6c488-130">The PS virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c488-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="6c488-131">-VMName</span></span>
<span data-ttu-id="6c488-132">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6c488-132">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="6c488-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c488-133">-Confirm</span></span>
<span data-ttu-id="6c488-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c488-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c488-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c488-135">-WhatIf</span></span>
<span data-ttu-id="6c488-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6c488-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c488-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6c488-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c488-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c488-138">CommonParameters</span></span>
<span data-ttu-id="6c488-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c488-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c488-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c488-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c488-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c488-141">INPUTS</span></span>

### <span data-ttu-id="6c488-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6c488-142">System.String</span></span>

### <span data-ttu-id="6c488-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6c488-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6c488-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6c488-144">OUTPUTS</span></span>

### <span data-ttu-id="6c488-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="6c488-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="6c488-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="6c488-146">NOTES</span></span>

## <span data-ttu-id="6c488-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c488-147">RELATED LINKS</span></span>
