---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 77ac953e1b67ea896f15b13a2695505aabc05bbb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115474"
---
# <span data-ttu-id="b5df7-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="b5df7-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="b5df7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5df7-102">SYNOPSIS</span></span>
<span data-ttu-id="b5df7-103">Execute um comando no VM.</span><span class="sxs-lookup"><span data-stu-id="b5df7-103">Run a command on the VM.</span></span>

## <span data-ttu-id="b5df7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5df7-104">SYNTAX</span></span>

### <span data-ttu-id="b5df7-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b5df7-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5df7-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b5df7-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5df7-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="b5df7-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5df7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5df7-108">DESCRIPTION</span></span>
<span data-ttu-id="b5df7-109">Invocar um comando executar no VM.</span><span class="sxs-lookup"><span data-stu-id="b5df7-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="b5df7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b5df7-110">EXAMPLES</span></span>

### <span data-ttu-id="b5df7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b5df7-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="b5df7-112">Invocar um comando de executar do RunPowerShellScript substituindo o script "sample.ps1" e os parâmetros no VM de 'vmname' no grupo de recursos 'rgname'.</span><span class="sxs-lookup"><span data-stu-id="b5df7-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="b5df7-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5df7-113">PARAMETERS</span></span>

### <span data-ttu-id="b5df7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5df7-114">-AsJob</span></span>
<span data-ttu-id="b5df7-115">Execute o cmdlet em segundo plano e retorne um objeto de trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="b5df7-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="b5df7-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="b5df7-116">-CommandId</span></span>
<span data-ttu-id="b5df7-117">A ID do comando Executar.</span><span class="sxs-lookup"><span data-stu-id="b5df7-117">The run command ID.</span></span>

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

### <span data-ttu-id="b5df7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5df7-118">-DefaultProfile</span></span>
<span data-ttu-id="b5df7-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5df7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5df7-120">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5df7-120">-Parameter</span></span>
<span data-ttu-id="b5df7-121">Os parâmetros de comando executar.</span><span class="sxs-lookup"><span data-stu-id="b5df7-121">The run command parameters.</span></span>

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

### <span data-ttu-id="b5df7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5df7-122">-ResourceGroupName</span></span>
<span data-ttu-id="b5df7-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b5df7-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="b5df7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5df7-124">-ResourceId</span></span>
<span data-ttu-id="b5df7-125">A ID do recurso do VM.</span><span class="sxs-lookup"><span data-stu-id="b5df7-125">The resource ID for the VM.</span></span>

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

### <span data-ttu-id="b5df7-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="b5df7-126">-ScriptPath</span></span>
<span data-ttu-id="b5df7-127">Caminho do script a ser executado.</span><span class="sxs-lookup"><span data-stu-id="b5df7-127">Path of the script to be executed.</span></span>  <span data-ttu-id="b5df7-128">Quando esse valor é dado, o script determinado substituirá o script padrão do comando.</span><span class="sxs-lookup"><span data-stu-id="b5df7-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="b5df7-129">-VM</span><span class="sxs-lookup"><span data-stu-id="b5df7-129">-VM</span></span>
<span data-ttu-id="b5df7-130">O objeto de máquina virtual PS.</span><span class="sxs-lookup"><span data-stu-id="b5df7-130">The PS virtual machine object.</span></span>

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

### <span data-ttu-id="b5df7-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="b5df7-131">-VMName</span></span>
<span data-ttu-id="b5df7-132">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b5df7-132">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="b5df7-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b5df7-133">-Confirm</span></span>
<span data-ttu-id="b5df7-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5df7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5df7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5df7-135">-WhatIf</span></span>
<span data-ttu-id="b5df7-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b5df7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5df7-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b5df7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5df7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5df7-138">CommonParameters</span></span>
<span data-ttu-id="b5df7-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5df7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5df7-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5df7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5df7-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="b5df7-141">INPUTS</span></span>

### <span data-ttu-id="b5df7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b5df7-142">System.String</span></span>

### <span data-ttu-id="b5df7-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b5df7-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b5df7-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="b5df7-144">OUTPUTS</span></span>

### <span data-ttu-id="b5df7-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="b5df7-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="b5df7-146">Notas</span><span class="sxs-lookup"><span data-stu-id="b5df7-146">NOTES</span></span>

## <span data-ttu-id="b5df7-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5df7-147">RELATED LINKS</span></span>
