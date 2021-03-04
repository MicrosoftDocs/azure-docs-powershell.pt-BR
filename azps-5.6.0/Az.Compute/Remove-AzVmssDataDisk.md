---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: abdef821862976a3bffb0b39bc48a3619e17d64f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891504"
---
# <span data-ttu-id="6b8ed-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="6b8ed-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="6b8ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="6b8ed-103">Remove um disco de dados do VMSS.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="6b8ed-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6b8ed-104">SYNTAX</span></span>

### <span data-ttu-id="6b8ed-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b8ed-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b8ed-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b8ed-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b8ed-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6b8ed-107">DESCRIPTION</span></span>
<span data-ttu-id="6b8ed-108">O cmdlet **Remove-AzVmssDataDisk** remove um disco de dados da instância do Conjunto de Escala de Máquina Virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="6b8ed-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="6b8ed-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b8ed-109">EXAMPLES</span></span>

### <span data-ttu-id="6b8ed-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6b8ed-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="6b8ed-111">Este comando remove o disco de dados chamado 'DataDisk1' do objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="6b8ed-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6b8ed-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="6b8ed-113">Este comando remove o disco de dados do LUN 0 do objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="6b8ed-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6b8ed-114">PARAMETERS</span></span>

### <span data-ttu-id="6b8ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b8ed-115">-DefaultProfile</span></span>
<span data-ttu-id="6b8ed-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b8ed-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="6b8ed-117">-Lun</span></span>
<span data-ttu-id="6b8ed-118">Especifica o número de unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="6b8ed-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6b8ed-119">-Name</span></span>
<span data-ttu-id="6b8ed-120">Especifica o nome do disco.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="6b8ed-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6b8ed-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6b8ed-122">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="6b8ed-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b8ed-123">-Confirm</span></span>
<span data-ttu-id="6b8ed-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b8ed-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b8ed-125">-WhatIf</span></span>
<span data-ttu-id="6b8ed-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b8ed-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b8ed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b8ed-128">CommonParameters</span></span>
<span data-ttu-id="6b8ed-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b8ed-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b8ed-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b8ed-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b8ed-131">INPUTS</span></span>

### <span data-ttu-id="6b8ed-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6b8ed-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="6b8ed-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6b8ed-133">System.String</span></span>

### <span data-ttu-id="6b8ed-134">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6b8ed-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6b8ed-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6b8ed-135">OUTPUTS</span></span>

### <span data-ttu-id="6b8ed-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6b8ed-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6b8ed-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="6b8ed-137">NOTES</span></span>

## <span data-ttu-id="6b8ed-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b8ed-138">RELATED LINKS</span></span>
