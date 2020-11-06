---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: b32734bbca2ec0fd554a073b2e0b5acf077874ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426960"
---
# <span data-ttu-id="47ae7-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="47ae7-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="47ae7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47ae7-102">SYNOPSIS</span></span>
<span data-ttu-id="47ae7-103">Remove um disco de dados do VMSS.</span><span class="sxs-lookup"><span data-stu-id="47ae7-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47ae7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47ae7-104">SYNTAX</span></span>

### <span data-ttu-id="47ae7-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47ae7-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47ae7-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="47ae7-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47ae7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47ae7-107">DESCRIPTION</span></span>
<span data-ttu-id="47ae7-108">O cmdlet **Remove-AzureRmVmssDataDisk** remove um disco de dados da instância VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="47ae7-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="47ae7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47ae7-109">EXAMPLES</span></span>

### <span data-ttu-id="47ae7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47ae7-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="47ae7-111">Esse comando Remove o disco de dados chamado ' datadisk1 ' do objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="47ae7-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="47ae7-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="47ae7-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="47ae7-113">Esse comando Remove o disco de dados do LUN 0 do objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="47ae7-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="47ae7-114">OS</span><span class="sxs-lookup"><span data-stu-id="47ae7-114">PARAMETERS</span></span>

### <span data-ttu-id="47ae7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ae7-115">-DefaultProfile</span></span>
<span data-ttu-id="47ae7-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47ae7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47ae7-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="47ae7-117">-Lun</span></span>
<span data-ttu-id="47ae7-118">Especifica o número de unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="47ae7-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="47ae7-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="47ae7-119">-Name</span></span>
<span data-ttu-id="47ae7-120">Especifica o nome do disco.</span><span class="sxs-lookup"><span data-stu-id="47ae7-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="47ae7-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="47ae7-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="47ae7-122">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="47ae7-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="47ae7-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47ae7-123">-Confirm</span></span>
<span data-ttu-id="47ae7-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47ae7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47ae7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47ae7-125">-WhatIf</span></span>
<span data-ttu-id="47ae7-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47ae7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47ae7-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47ae7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47ae7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ae7-128">CommonParameters</span></span>
<span data-ttu-id="47ae7-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47ae7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ae7-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47ae7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ae7-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47ae7-131">INPUTS</span></span>

### <span data-ttu-id="47ae7-132">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="47ae7-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="47ae7-133">System. String System. Nullable ' 1 [System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="47ae7-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="47ae7-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47ae7-134">OUTPUTS</span></span>

### <span data-ttu-id="47ae7-135">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="47ae7-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="47ae7-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47ae7-136">NOTES</span></span>

## <span data-ttu-id="47ae7-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47ae7-137">RELATED LINKS</span></span>

