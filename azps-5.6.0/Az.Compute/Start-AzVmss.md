---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 2ff37cec23499afb0a0bb14069dc4e694f4440f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887815"
---
# <span data-ttu-id="6ee1f-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ee1f-101">Start-AzVmss</span></span>

## <span data-ttu-id="6ee1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ee1f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ee1f-103">Inicia o VMSS ou um conjunto de máquinas virtuais no VMSS.</span><span class="sxs-lookup"><span data-stu-id="6ee1f-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="6ee1f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6ee1f-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ee1f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6ee1f-105">DESCRIPTION</span></span>
<span data-ttu-id="6ee1f-106">O cmdlet **Start-AzVmss** inicia todas as máquinas virtuais dentro do Conjunto de Escala de Máquina Virtual (VMSS) ou um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="6ee1f-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="6ee1f-107">Você pode usar o *parâmetro InstanceId* para selecionar um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="6ee1f-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="6ee1f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ee1f-108">EXAMPLES</span></span>

### <span data-ttu-id="6ee1f-109">Exemplo 1: Iniciar um conjunto específico de máquinas virtuais no VMSS</span><span class="sxs-lookup"><span data-stu-id="6ee1f-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="6ee1f-110">Este comando inicia um conjunto específico de máquinas virtuais especificadas pela matriz de cadeia de caracteres de ID de instância que pertencem à VMSS chamada ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="6ee1f-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="6ee1f-111">Exemplo 2: Iniciar todas as máquinas virtuais no VMSS</span><span class="sxs-lookup"><span data-stu-id="6ee1f-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="6ee1f-112">Este comando inicia todas as máquinas virtuais que pertencem à VMSS chamada ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="6ee1f-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="6ee1f-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6ee1f-113">PARAMETERS</span></span>

### <span data-ttu-id="6ee1f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ee1f-114">-AsJob</span></span>
<span data-ttu-id="6ee1f-115">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="6ee1f-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6ee1f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ee1f-116">-DefaultProfile</span></span>
<span data-ttu-id="6ee1f-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6ee1f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ee1f-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="6ee1f-118">-InstanceId</span></span>
<span data-ttu-id="6ee1f-119">Especifica, como uma matriz de cadeia de caracteres, a ID ou IDs das instâncias que o cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="6ee1f-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="6ee1f-120">Por exemplo: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="6ee1f-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="6ee1f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ee1f-121">-ResourceGroupName</span></span>
<span data-ttu-id="6ee1f-122">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="6ee1f-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="6ee1f-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6ee1f-123">-VMScaleSetName</span></span>
<span data-ttu-id="6ee1f-124">Especifica o nome do VMSS que este cmdlet inicia as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="6ee1f-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="6ee1f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ee1f-125">-Confirm</span></span>
<span data-ttu-id="6ee1f-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ee1f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ee1f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ee1f-127">-WhatIf</span></span>
<span data-ttu-id="6ee1f-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6ee1f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ee1f-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6ee1f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ee1f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ee1f-130">CommonParameters</span></span>
<span data-ttu-id="6ee1f-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ee1f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ee1f-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ee1f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ee1f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ee1f-133">INPUTS</span></span>

### <span data-ttu-id="6ee1f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6ee1f-134">System.String</span></span>

### <span data-ttu-id="6ee1f-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6ee1f-135">System.String[]</span></span>

## <span data-ttu-id="6ee1f-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6ee1f-136">OUTPUTS</span></span>

### <span data-ttu-id="6ee1f-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6ee1f-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6ee1f-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="6ee1f-138">NOTES</span></span>

## <span data-ttu-id="6ee1f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ee1f-139">RELATED LINKS</span></span>

[<span data-ttu-id="6ee1f-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ee1f-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="6ee1f-141">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ee1f-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="6ee1f-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ee1f-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="6ee1f-143">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ee1f-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="6ee1f-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ee1f-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="6ee1f-145">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ee1f-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="6ee1f-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ee1f-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


