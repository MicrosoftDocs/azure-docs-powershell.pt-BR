---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 5ceb420f30525817ebccd6d3f38a53e6c1cad66e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776812"
---
# <span data-ttu-id="8c3dd-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8c3dd-101">Set-AzVmss</span></span>

## <span data-ttu-id="8c3dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="8c3dd-103">Define ações específicas em um VMSS especificado.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="8c3dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c3dd-104">SYNTAX</span></span>

### <span data-ttu-id="8c3dd-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="8c3dd-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c3dd-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="8c3dd-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c3dd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c3dd-107">DESCRIPTION</span></span>
<span data-ttu-id="8c3dd-108">O cmdlet **set-AzVmss** define ações específicas no conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8c3dd-108">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="8c3dd-109">A única ação aceita por este cmdlet é a reimagem.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="8c3dd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c3dd-110">EXAMPLES</span></span>

### <span data-ttu-id="8c3dd-111">Exemplo 1: reimagem de um VMSS</span><span class="sxs-lookup"><span data-stu-id="8c3dd-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="8c3dd-112">Esse comando faz a nova imagem do VMSS chamado ContosoVMSS que pertence ao grupo de recursos chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="8c3dd-113">OS</span><span class="sxs-lookup"><span data-stu-id="8c3dd-113">PARAMETERS</span></span>

### <span data-ttu-id="8c3dd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c3dd-114">-AsJob</span></span>
<span data-ttu-id="8c3dd-115">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8c3dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c3dd-116">-DefaultProfile</span></span>
<span data-ttu-id="8c3dd-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c3dd-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="8c3dd-118">-InstanceId</span></span>
<span data-ttu-id="8c3dd-119">A ID de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-119">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="8c3dd-120">-Nova imagem</span><span class="sxs-lookup"><span data-stu-id="8c3dd-120">-Reimage</span></span>
<span data-ttu-id="8c3dd-121">Indica que o cmdlet reimagemia o VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-121">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c3dd-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="8c3dd-122">-ReimageAll</span></span>
<span data-ttu-id="8c3dd-123">Indica que o cmdlet reimagemia todos os discos no VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c3dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c3dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="8c3dd-125">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="8c3dd-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8c3dd-126">-VMScaleSetName</span></span>
<span data-ttu-id="8c3dd-127">Especifica o nome do VMSS para o qual esse cmdlet define ações.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="8c3dd-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8c3dd-128">-Confirm</span></span>
<span data-ttu-id="8c3dd-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c3dd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c3dd-130">-WhatIf</span></span>
<span data-ttu-id="8c3dd-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c3dd-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c3dd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c3dd-133">CommonParameters</span></span>
<span data-ttu-id="8c3dd-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c3dd-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c3dd-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c3dd-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c3dd-136">INPUTS</span></span>

### <span data-ttu-id="8c3dd-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8c3dd-137">None</span></span>
<span data-ttu-id="8c3dd-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c3dd-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c3dd-139">OUTPUTS</span></span>

### <span data-ttu-id="8c3dd-140">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8c3dd-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8c3dd-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c3dd-141">NOTES</span></span>

## <span data-ttu-id="8c3dd-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c3dd-142">RELATED LINKS</span></span>

[<span data-ttu-id="8c3dd-143">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8c3dd-143">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="8c3dd-144">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8c3dd-144">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="8c3dd-145">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8c3dd-145">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="8c3dd-146">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8c3dd-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="8c3dd-147">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8c3dd-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="8c3dd-148">Parar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8c3dd-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="8c3dd-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8c3dd-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


