---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: 2ed7be0cf790a596a2a2fc9b23c0e6aa50f67623
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891506"
---
# <span data-ttu-id="b3c9c-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b3c9c-101">Remove-AzVmss</span></span>

## <span data-ttu-id="b3c9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c9c-103">Remove o VMSS ou uma máquina virtual que está dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="b3c9c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b3c9c-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3c9c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b3c9c-105">DESCRIPTION</span></span>
<span data-ttu-id="b3c9c-106">O cmdlet **Remove-AzVmss** remove o Conjunto de Escala de Máquina Virtual (VMSS) do Azure.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="b3c9c-107">Esse cmdlet também pode ser usado para remover uma máquina virtual específica dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="b3c9c-108">Você pode usar o *parâmetro InstanceId* para remover uma máquina virtual específica dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="b3c9c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3c9c-109">EXAMPLES</span></span>

### <span data-ttu-id="b3c9c-110">Exemplo 1: Remover um VMSS</span><span class="sxs-lookup"><span data-stu-id="b3c9c-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="b3c9c-111">Este comando remove o VMSS chamado VMScaleSet001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="b3c9c-112">Exemplo 2: Remover uma máquina virtual de dentro de um VMSS</span><span class="sxs-lookup"><span data-stu-id="b3c9c-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="b3c9c-113">Este comando remove a máquina virtual com a ID da instância 3 do VMSS chamado VMScaleSet002 que pertence ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="b3c9c-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b3c9c-114">PARAMETERS</span></span>

### <span data-ttu-id="b3c9c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3c9c-115">-AsJob</span></span>
<span data-ttu-id="b3c9c-116">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b3c9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c9c-117">-DefaultProfile</span></span>
<span data-ttu-id="b3c9c-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3c9c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b3c9c-119">-Force</span></span>
<span data-ttu-id="b3c9c-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b3c9c-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b3c9c-121">-InstanceId</span></span>
<span data-ttu-id="b3c9c-122">Especifica, como uma matriz de cadeia de caracteres, a ID das instâncias que precisam ser iniciadas.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="b3c9c-123">Por exemplo: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="b3c9c-123">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c9c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3c9c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3c9c-125">Especifica o nome do grupo de recursos ao que o VMSS pertence.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c9c-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b3c9c-126">-VMScaleSetName</span></span>
<span data-ttu-id="b3c9c-127">Especiem o nome do VMSS que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="b3c9c-128">Se você especificar o *parâmetro InstanceId,* o cmdlet removerá a máquina virtual especificada do VMSS nomeado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c9c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3c9c-129">-Confirm</span></span>
<span data-ttu-id="b3c9c-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c9c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3c9c-131">-WhatIf</span></span>
<span data-ttu-id="b3c9c-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3c9c-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c9c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c9c-134">CommonParameters</span></span>
<span data-ttu-id="b3c9c-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3c9c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c9c-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3c9c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c9c-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3c9c-137">INPUTS</span></span>

### <span data-ttu-id="b3c9c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b3c9c-138">System.String</span></span>

### <span data-ttu-id="b3c9c-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b3c9c-139">System.String[]</span></span>

## <span data-ttu-id="b3c9c-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b3c9c-140">OUTPUTS</span></span>

### <span data-ttu-id="b3c9c-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b3c9c-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b3c9c-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="b3c9c-142">NOTES</span></span>

## <span data-ttu-id="b3c9c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3c9c-143">RELATED LINKS</span></span>

[<span data-ttu-id="b3c9c-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b3c9c-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="b3c9c-145">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b3c9c-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="b3c9c-146">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b3c9c-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="b3c9c-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b3c9c-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="b3c9c-148">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b3c9c-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="b3c9c-149">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b3c9c-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="b3c9c-150">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b3c9c-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


