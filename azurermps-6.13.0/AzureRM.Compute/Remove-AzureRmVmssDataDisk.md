---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: 1e0c04bd7283bc2a741b5e2a7130e83b35d00133
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433295"
---
# <span data-ttu-id="c3a9c-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="c3a9c-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="c3a9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="c3a9c-103">Remove um disco de dados do VMSS.</span><span class="sxs-lookup"><span data-stu-id="c3a9c-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3a9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3a9c-104">SYNTAX</span></span>

### <span data-ttu-id="c3a9c-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3a9c-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3a9c-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3a9c-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3a9c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3a9c-107">DESCRIPTION</span></span>
<span data-ttu-id="c3a9c-108">O cmdlet **Remove-AzureRmVmssDataDisk** remove um disco de dados da instância VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="c3a9c-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="c3a9c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3a9c-109">EXAMPLES</span></span>

### <span data-ttu-id="c3a9c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3a9c-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="c3a9c-111">Esse comando Remove o disco de dados chamado ' datadisk1 ' do objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="c3a9c-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="c3a9c-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c3a9c-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="c3a9c-113">Esse comando Remove o disco de dados do LUN 0 do objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="c3a9c-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="c3a9c-114">OS</span><span class="sxs-lookup"><span data-stu-id="c3a9c-114">PARAMETERS</span></span>

### <span data-ttu-id="c3a9c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3a9c-115">-DefaultProfile</span></span>
<span data-ttu-id="c3a9c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3a9c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3a9c-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="c3a9c-117">-Lun</span></span>
<span data-ttu-id="c3a9c-118">Especifica o número de unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="c3a9c-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3a9c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3a9c-119">-Name</span></span>
<span data-ttu-id="c3a9c-120">Especifica o nome do disco.</span><span class="sxs-lookup"><span data-stu-id="c3a9c-120">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3a9c-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c3a9c-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c3a9c-122">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="c3a9c-122">Specify the VMSS object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3a9c-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c3a9c-123">-Confirm</span></span>
<span data-ttu-id="c3a9c-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3a9c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3a9c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3a9c-125">-WhatIf</span></span>
<span data-ttu-id="c3a9c-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3a9c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3a9c-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3a9c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3a9c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3a9c-128">CommonParameters</span></span>
<span data-ttu-id="c3a9c-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3a9c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3a9c-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3a9c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3a9c-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3a9c-131">INPUTS</span></span>

### <span data-ttu-id="c3a9c-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c3a9c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="c3a9c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c3a9c-133">System.String</span></span>

### <span data-ttu-id="c3a9c-134">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c3a9c-134">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c3a9c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3a9c-135">OUTPUTS</span></span>

### <span data-ttu-id="c3a9c-136">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c3a9c-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c3a9c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3a9c-137">NOTES</span></span>

## <span data-ttu-id="c3a9c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3a9c-138">RELATED LINKS</span></span>
