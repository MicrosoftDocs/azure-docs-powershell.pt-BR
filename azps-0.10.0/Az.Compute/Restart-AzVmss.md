---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: b0e01f462bfb7576e942138cb42b3171fb6660b3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776884"
---
# <span data-ttu-id="4480f-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4480f-101">Restart-AzVmss</span></span>

## <span data-ttu-id="4480f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4480f-102">SYNOPSIS</span></span>
<span data-ttu-id="4480f-103">Reinicia o VMSS ou uma máquina virtual dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="4480f-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="4480f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4480f-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4480f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4480f-105">DESCRIPTION</span></span>
<span data-ttu-id="4480f-106">O cmdlet **Restart-AzVmss** reinicia o conjunto de dimensionamento da máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="4480f-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="4480f-107">Esse cmdlet também pode ser usado para reiniciar uma máquina virtual específica dentro do VMSS usando o parâmetro *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="4480f-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="4480f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4480f-108">EXAMPLES</span></span>

### <span data-ttu-id="4480f-109">Exemplo 1: reiniciar o VMSS</span><span class="sxs-lookup"><span data-stu-id="4480f-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="4480f-110">Esse comando reinicia o VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="4480f-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="4480f-111">Exemplo 2: reiniciar uma máquina virtual específica dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="4480f-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="4480f-112">Esse comando reinicia uma máquina virtual com a ID de instância 1 no VMSS chamada VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="4480f-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="4480f-113">OS</span><span class="sxs-lookup"><span data-stu-id="4480f-113">PARAMETERS</span></span>

### <span data-ttu-id="4480f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4480f-114">-AsJob</span></span>
<span data-ttu-id="4480f-115">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="4480f-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4480f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4480f-116">-DefaultProfile</span></span>
<span data-ttu-id="4480f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4480f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4480f-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="4480f-118">-InstanceId</span></span>
<span data-ttu-id="4480f-119">Especifica, como uma matriz de cadeia de caracteres, a ID das instâncias que precisam ser reiniciadas.</span><span class="sxs-lookup"><span data-stu-id="4480f-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="4480f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4480f-120">-ResourceGroupName</span></span>
<span data-ttu-id="4480f-121">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="4480f-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="4480f-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4480f-122">-VMScaleSetName</span></span>
<span data-ttu-id="4480f-123">Especifica o nome do VMSS que este cmdlet reinicia.</span><span class="sxs-lookup"><span data-stu-id="4480f-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="4480f-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4480f-124">-Confirm</span></span>
<span data-ttu-id="4480f-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4480f-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4480f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4480f-126">-WhatIf</span></span>
<span data-ttu-id="4480f-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4480f-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4480f-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4480f-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4480f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4480f-129">CommonParameters</span></span>
<span data-ttu-id="4480f-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4480f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4480f-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4480f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4480f-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4480f-132">INPUTS</span></span>

### <span data-ttu-id="4480f-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4480f-133">None</span></span>
<span data-ttu-id="4480f-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4480f-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4480f-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4480f-135">OUTPUTS</span></span>

###  
<span data-ttu-id="4480f-136">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="4480f-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="4480f-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4480f-137">NOTES</span></span>

## <span data-ttu-id="4480f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4480f-138">RELATED LINKS</span></span>

[<span data-ttu-id="4480f-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4480f-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="4480f-140">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4480f-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="4480f-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4480f-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="4480f-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4480f-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="4480f-143">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4480f-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="4480f-144">Parar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4480f-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="4480f-145">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4480f-145">Update-AzVmss</span></span>](./Update-AzVmss.md)


