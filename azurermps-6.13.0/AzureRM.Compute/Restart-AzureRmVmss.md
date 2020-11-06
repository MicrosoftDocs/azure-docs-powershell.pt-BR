---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 9f4727fc9bc5a735f837d3bec5eced9cd20e9254
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610620"
---
# <span data-ttu-id="e17f1-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e17f1-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="e17f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e17f1-102">SYNOPSIS</span></span>
<span data-ttu-id="e17f1-103">Reinicia o VMSS ou uma máquina virtual dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="e17f1-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e17f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e17f1-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e17f1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e17f1-105">DESCRIPTION</span></span>
<span data-ttu-id="e17f1-106">O cmdlet **Restart-AzureRmVmss** reinicia o conjunto de dimensionamento da máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="e17f1-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="e17f1-107">Esse cmdlet também pode ser usado para reiniciar uma máquina virtual específica dentro do VMSS usando o parâmetro *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="e17f1-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="e17f1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e17f1-108">EXAMPLES</span></span>

### <span data-ttu-id="e17f1-109">Exemplo 1: reiniciar o VMSS</span><span class="sxs-lookup"><span data-stu-id="e17f1-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="e17f1-110">Esse comando reinicia o VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="e17f1-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="e17f1-111">Exemplo 2: reiniciar uma máquina virtual específica dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="e17f1-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="e17f1-112">Esse comando reinicia uma máquina virtual com a ID de instância 1 no VMSS chamada VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="e17f1-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="e17f1-113">OS</span><span class="sxs-lookup"><span data-stu-id="e17f1-113">PARAMETERS</span></span>

### <span data-ttu-id="e17f1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e17f1-114">-AsJob</span></span>
<span data-ttu-id="e17f1-115">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="e17f1-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e17f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e17f1-116">-DefaultProfile</span></span>
<span data-ttu-id="e17f1-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e17f1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17f1-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e17f1-118">-InstanceId</span></span>
<span data-ttu-id="e17f1-119">Especifica, como uma matriz de cadeia de caracteres, a ID das instâncias que precisam ser reiniciadas.</span><span class="sxs-lookup"><span data-stu-id="e17f1-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17f1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e17f1-120">-ResourceGroupName</span></span>
<span data-ttu-id="e17f1-121">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="e17f1-121">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17f1-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e17f1-122">-VMScaleSetName</span></span>
<span data-ttu-id="e17f1-123">Especifica o nome do VMSS que este cmdlet reinicia.</span><span class="sxs-lookup"><span data-stu-id="e17f1-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17f1-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e17f1-124">-Confirm</span></span>
<span data-ttu-id="e17f1-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e17f1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e17f1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e17f1-126">-WhatIf</span></span>
<span data-ttu-id="e17f1-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e17f1-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e17f1-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e17f1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e17f1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e17f1-129">CommonParameters</span></span>
<span data-ttu-id="e17f1-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e17f1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e17f1-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e17f1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e17f1-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e17f1-132">INPUTS</span></span>

### <span data-ttu-id="e17f1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e17f1-133">System.String</span></span>

### <span data-ttu-id="e17f1-134">System. String []</span><span class="sxs-lookup"><span data-stu-id="e17f1-134">System.String[]</span></span>

## <span data-ttu-id="e17f1-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e17f1-135">OUTPUTS</span></span>

### <span data-ttu-id="e17f1-136">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e17f1-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e17f1-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e17f1-137">NOTES</span></span>

## <span data-ttu-id="e17f1-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e17f1-138">RELATED LINKS</span></span>

[<span data-ttu-id="e17f1-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e17f1-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="e17f1-140">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e17f1-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="e17f1-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e17f1-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="e17f1-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e17f1-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="e17f1-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e17f1-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="e17f1-144">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e17f1-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="e17f1-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e17f1-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


