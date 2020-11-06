---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: e4c3199218294e1a75a2bc62dd148c3409159ed7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427997"
---
# <span data-ttu-id="f811d-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="f811d-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="f811d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f811d-102">SYNOPSIS</span></span>
<span data-ttu-id="f811d-103">Modifica o estado de uma instância de VMSS.</span><span class="sxs-lookup"><span data-stu-id="f811d-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f811d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f811d-104">SYNTAX</span></span>

### <span data-ttu-id="f811d-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="f811d-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f811d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="f811d-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f811d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f811d-107">DESCRIPTION</span></span>
<span data-ttu-id="f811d-108">O cmdlet **set-AzureRmVmssVM** modifica o estado de uma instância de VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="f811d-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="f811d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f811d-109">EXAMPLES</span></span>

## <span data-ttu-id="f811d-110">OS</span><span class="sxs-lookup"><span data-stu-id="f811d-110">PARAMETERS</span></span>

### <span data-ttu-id="f811d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f811d-111">-DefaultProfile</span></span>
<span data-ttu-id="f811d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f811d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f811d-113">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f811d-113">-InstanceId</span></span>
<span data-ttu-id="f811d-114">Especifica a ID da instância VMSS para a qual esse cmdlet modifica o estado.</span><span class="sxs-lookup"><span data-stu-id="f811d-114">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f811d-115">-Nova imagem</span><span class="sxs-lookup"><span data-stu-id="f811d-115">-Reimage</span></span>
<span data-ttu-id="f811d-116">Indica que esse cmdlet reimagemia a instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="f811d-116">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f811d-117">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="f811d-117">-ReimageAll</span></span>
<span data-ttu-id="f811d-118">Indica que o cmdlet reimagemia todos os discos na instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="f811d-118">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f811d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f811d-119">-ResourceGroupName</span></span>
<span data-ttu-id="f811d-120">Especifica o nome do grupo de recursos que contém a instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="f811d-120">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="f811d-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f811d-121">-VMScaleSetName</span></span>
<span data-ttu-id="f811d-122">Especifica o nome da instância VMSS que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="f811d-122">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f811d-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f811d-123">-Confirm</span></span>
<span data-ttu-id="f811d-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f811d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f811d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f811d-125">-WhatIf</span></span>
<span data-ttu-id="f811d-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f811d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f811d-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f811d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f811d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f811d-128">CommonParameters</span></span>
<span data-ttu-id="f811d-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f811d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f811d-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f811d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f811d-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f811d-131">INPUTS</span></span>

## <span data-ttu-id="f811d-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f811d-132">OUTPUTS</span></span>

## <span data-ttu-id="f811d-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f811d-133">NOTES</span></span>

## <span data-ttu-id="f811d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f811d-134">RELATED LINKS</span></span>

[<span data-ttu-id="f811d-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="f811d-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
