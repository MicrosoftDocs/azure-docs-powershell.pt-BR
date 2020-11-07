---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: c8de667ae818749e980d3e917838717ec3c85b07
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776901"
---
# <span data-ttu-id="d075e-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d075e-101">Remove-AzVmss</span></span>

## <span data-ttu-id="d075e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d075e-102">SYNOPSIS</span></span>
<span data-ttu-id="d075e-103">Remove o VMSS ou uma máquina virtual que está dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="d075e-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="d075e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d075e-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d075e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d075e-105">DESCRIPTION</span></span>
<span data-ttu-id="d075e-106">O cmdlet **Remove-AzVmss** remove o VMSS (conjunto de escala da máquina virtual) do Azure.</span><span class="sxs-lookup"><span data-stu-id="d075e-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="d075e-107">Esse cmdlet também pode ser usado para remover uma máquina virtual específica dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="d075e-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="d075e-108">Você pode usar o parâmetro *InstanceId* para remover uma máquina virtual específica dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="d075e-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="d075e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d075e-109">EXAMPLES</span></span>

### <span data-ttu-id="d075e-110">Exemplo 1: remover um VMSS</span><span class="sxs-lookup"><span data-stu-id="d075e-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="d075e-111">Esse comando Remove a VMSS chamada VMScaleSet001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="d075e-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="d075e-112">Exemplo 2: remover uma máquina virtual de dentro de um VMSS</span><span class="sxs-lookup"><span data-stu-id="d075e-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="d075e-113">Esse comando Remove a máquina virtual com a ID de instância 3 da VMSS chamada VMScaleSet002 que pertence ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="d075e-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="d075e-114">OS</span><span class="sxs-lookup"><span data-stu-id="d075e-114">PARAMETERS</span></span>

### <span data-ttu-id="d075e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d075e-115">-AsJob</span></span>
<span data-ttu-id="d075e-116">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="d075e-116">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d075e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d075e-117">-DefaultProfile</span></span>
<span data-ttu-id="d075e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d075e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d075e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d075e-119">-Force</span></span>
<span data-ttu-id="d075e-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d075e-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d075e-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d075e-121">-InstanceId</span></span>
<span data-ttu-id="d075e-122">Especifica, como uma matriz de cadeia de caracteres, a ID das instâncias que precisam ser iniciadas.</span><span class="sxs-lookup"><span data-stu-id="d075e-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="d075e-123">Por exemplo: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="d075e-123">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d075e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d075e-124">-ResourceGroupName</span></span>
<span data-ttu-id="d075e-125">Especifica o nome do grupo de recursos ao qual o VMSS pertence.</span><span class="sxs-lookup"><span data-stu-id="d075e-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d075e-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d075e-126">-VMScaleSetName</span></span>
<span data-ttu-id="d075e-127">Especifica o nome do VMSS que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="d075e-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="d075e-128">Se você especificar o parâmetro *InstanceId* , o cmdlet removerá a máquina virtual especificada do VMSS nomeado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d075e-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d075e-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d075e-129">-Confirm</span></span>
<span data-ttu-id="d075e-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d075e-130">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d075e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d075e-131">-WhatIf</span></span>
<span data-ttu-id="d075e-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d075e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d075e-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d075e-133">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d075e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d075e-134">CommonParameters</span></span>
<span data-ttu-id="d075e-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d075e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d075e-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d075e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d075e-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d075e-137">INPUTS</span></span>

### <span data-ttu-id="d075e-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d075e-138">None</span></span>
<span data-ttu-id="d075e-139">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d075e-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d075e-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d075e-140">OUTPUTS</span></span>

### <span data-ttu-id="d075e-141">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d075e-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d075e-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d075e-142">NOTES</span></span>

## <span data-ttu-id="d075e-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d075e-143">RELATED LINKS</span></span>

[<span data-ttu-id="d075e-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d075e-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="d075e-145">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d075e-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="d075e-146">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d075e-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="d075e-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d075e-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="d075e-148">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d075e-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="d075e-149">Parar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d075e-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="d075e-150">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d075e-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


