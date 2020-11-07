---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 30836628d6be41e06eaf8982fcc59646fb5b5e89
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776897"
---
# <span data-ttu-id="6026b-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="6026b-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="6026b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6026b-102">SYNOPSIS</span></span>
<span data-ttu-id="6026b-103">Remove um disco de dados do VMSS.</span><span class="sxs-lookup"><span data-stu-id="6026b-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="6026b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6026b-104">SYNTAX</span></span>

### <span data-ttu-id="6026b-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6026b-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6026b-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="6026b-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6026b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6026b-107">DESCRIPTION</span></span>
<span data-ttu-id="6026b-108">O cmdlet **Remove-AzVmssDataDisk** remove um disco de dados da instância VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="6026b-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="6026b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6026b-109">EXAMPLES</span></span>

### <span data-ttu-id="6026b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6026b-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="6026b-111">Esse comando Remove o disco de dados chamado ' datadisk1 ' do objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="6026b-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="6026b-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6026b-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="6026b-113">Esse comando Remove o disco de dados do LUN 0 do objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="6026b-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="6026b-114">OS</span><span class="sxs-lookup"><span data-stu-id="6026b-114">PARAMETERS</span></span>

### <span data-ttu-id="6026b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6026b-115">-DefaultProfile</span></span>
<span data-ttu-id="6026b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6026b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6026b-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="6026b-117">-Lun</span></span>
<span data-ttu-id="6026b-118">Especifica o número de unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="6026b-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6026b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6026b-119">-Name</span></span>
<span data-ttu-id="6026b-120">Especifica o nome do disco.</span><span class="sxs-lookup"><span data-stu-id="6026b-120">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6026b-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6026b-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6026b-122">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="6026b-122">Specify the VMSS object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6026b-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6026b-123">-Confirm</span></span>
<span data-ttu-id="6026b-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6026b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6026b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6026b-125">-WhatIf</span></span>
<span data-ttu-id="6026b-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6026b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6026b-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6026b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6026b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6026b-128">CommonParameters</span></span>
<span data-ttu-id="6026b-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6026b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6026b-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6026b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6026b-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6026b-131">INPUTS</span></span>

### <span data-ttu-id="6026b-132">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6026b-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="6026b-133">System. String System. Nullable ' 1 [System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6026b-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6026b-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6026b-134">OUTPUTS</span></span>

### <span data-ttu-id="6026b-135">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6026b-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="6026b-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6026b-136">NOTES</span></span>

## <span data-ttu-id="6026b-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6026b-137">RELATED LINKS</span></span>

