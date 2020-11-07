---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssvm
schema: 2.0.0
ms.openlocfilehash: ffce87e30fb5bffa78cb10a85b1ac8a143deeaad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786552"
---
# <span data-ttu-id="a7f93-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="a7f93-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="a7f93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7f93-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f93-103">Modifica o estado de uma instância de VMSS.</span><span class="sxs-lookup"><span data-stu-id="a7f93-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7f93-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7f93-104">SYNTAX</span></span>

### <span data-ttu-id="a7f93-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="a7f93-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7f93-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="a7f93-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7f93-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7f93-107">DESCRIPTION</span></span>
<span data-ttu-id="a7f93-108">O cmdlet **set-AzureRmVmssVM** modifica o estado de uma instância de VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="a7f93-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="a7f93-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7f93-109">EXAMPLES</span></span>

## <span data-ttu-id="a7f93-110">OS</span><span class="sxs-lookup"><span data-stu-id="a7f93-110">PARAMETERS</span></span>

### <span data-ttu-id="a7f93-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7f93-111">-AsJob</span></span>
<span data-ttu-id="a7f93-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a7f93-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7f93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f93-113">-DefaultProfile</span></span>
<span data-ttu-id="a7f93-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f93-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7f93-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a7f93-115">-InstanceId</span></span>
<span data-ttu-id="a7f93-116">Especifica a ID da instância VMSS para a qual esse cmdlet modifica o estado.</span><span class="sxs-lookup"><span data-stu-id="a7f93-116">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

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

### <span data-ttu-id="a7f93-117">-Nova imagem</span><span class="sxs-lookup"><span data-stu-id="a7f93-117">-Reimage</span></span>
<span data-ttu-id="a7f93-118">Indica que esse cmdlet reimagemia a instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="a7f93-118">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="a7f93-119">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="a7f93-119">-ReimageAll</span></span>
<span data-ttu-id="a7f93-120">Indica que o cmdlet reimagemia todos os discos na instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="a7f93-120">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="a7f93-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f93-121">-ResourceGroupName</span></span>
<span data-ttu-id="a7f93-122">Especifica o nome do grupo de recursos que contém a instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="a7f93-122">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="a7f93-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a7f93-123">-VMScaleSetName</span></span>
<span data-ttu-id="a7f93-124">Especifica o nome da instância VMSS que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="a7f93-124">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a7f93-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a7f93-125">-Confirm</span></span>
<span data-ttu-id="a7f93-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7f93-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7f93-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7f93-127">-WhatIf</span></span>
<span data-ttu-id="a7f93-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a7f93-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7f93-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7f93-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7f93-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f93-130">CommonParameters</span></span>
<span data-ttu-id="a7f93-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f93-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f93-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7f93-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f93-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7f93-133">INPUTS</span></span>

### <span data-ttu-id="a7f93-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a7f93-134">None</span></span>
<span data-ttu-id="a7f93-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a7f93-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7f93-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7f93-136">OUTPUTS</span></span>

### <span data-ttu-id="a7f93-137">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a7f93-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a7f93-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7f93-138">NOTES</span></span>

## <span data-ttu-id="a7f93-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7f93-139">RELATED LINKS</span></span>

[<span data-ttu-id="a7f93-140">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="a7f93-140">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
