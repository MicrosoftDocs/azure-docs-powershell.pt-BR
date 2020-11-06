---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: d035844046e238694cfec72feda9eab61b7714d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431042"
---
# <span data-ttu-id="c7254-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="c7254-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="c7254-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7254-102">SYNOPSIS</span></span>
<span data-ttu-id="c7254-103">Modifica o estado de uma instância de VMSS.</span><span class="sxs-lookup"><span data-stu-id="c7254-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7254-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7254-104">SYNTAX</span></span>

### <span data-ttu-id="c7254-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="c7254-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7254-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="c7254-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7254-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7254-107">DESCRIPTION</span></span>
<span data-ttu-id="c7254-108">O cmdlet **set-AzureRmVmssVM** modifica o estado de uma instância de VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="c7254-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="c7254-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7254-109">EXAMPLES</span></span>

## <span data-ttu-id="c7254-110">OS</span><span class="sxs-lookup"><span data-stu-id="c7254-110">PARAMETERS</span></span>

### <span data-ttu-id="c7254-111">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c7254-111">-InstanceId</span></span>
<span data-ttu-id="c7254-112">Especifica a ID da instância VMSS para a qual esse cmdlet modifica o estado.</span><span class="sxs-lookup"><span data-stu-id="c7254-112">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7254-113">-Nova imagem</span><span class="sxs-lookup"><span data-stu-id="c7254-113">-Reimage</span></span>
<span data-ttu-id="c7254-114">Indica que esse cmdlet reimagemia a instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="c7254-114">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7254-115">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="c7254-115">-ReimageAll</span></span>
<span data-ttu-id="c7254-116">Indica que o cmdlet reimagemia todos os discos na instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="c7254-116">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7254-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7254-117">-ResourceGroupName</span></span>
<span data-ttu-id="c7254-118">Especifica o nome do grupo de recursos que contém a instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="c7254-118">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="c7254-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c7254-119">-VMScaleSetName</span></span>
<span data-ttu-id="c7254-120">Especifica o nome da instância VMSS que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="c7254-120">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c7254-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c7254-121">-Confirm</span></span>
<span data-ttu-id="c7254-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7254-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7254-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7254-123">-WhatIf</span></span>
<span data-ttu-id="c7254-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c7254-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7254-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c7254-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7254-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7254-126">CommonParameters</span></span>
<span data-ttu-id="c7254-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7254-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7254-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7254-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7254-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7254-129">INPUTS</span></span>

### <span data-ttu-id="c7254-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c7254-130">None</span></span>
<span data-ttu-id="c7254-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c7254-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7254-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7254-132">OUTPUTS</span></span>

## <span data-ttu-id="c7254-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7254-133">NOTES</span></span>

## <span data-ttu-id="c7254-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7254-134">RELATED LINKS</span></span>

[<span data-ttu-id="c7254-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="c7254-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
