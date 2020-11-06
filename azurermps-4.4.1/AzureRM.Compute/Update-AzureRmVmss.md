---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 44022fe8ea12c8f341952bd023aa41bf4ead92c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431786"
---
# <span data-ttu-id="75d57-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="75d57-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="75d57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75d57-102">SYNOPSIS</span></span>
<span data-ttu-id="75d57-103">Atualiza o estado de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="75d57-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75d57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75d57-104">SYNTAX</span></span>

```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75d57-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75d57-105">DESCRIPTION</span></span>
<span data-ttu-id="75d57-106">O cmdlet **Update-AzureRmVmss** atualiza o estado de um VMSS (conjunto de dimensionamento de máquina virtual) para o estado de um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="75d57-106">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="75d57-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75d57-107">EXAMPLES</span></span>

### <span data-ttu-id="75d57-108">Exemplo 1: Atualize o estado de um VMSS para o estado de um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="75d57-108">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

<span data-ttu-id="75d57-109">Esse comando atualiza o estado do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001 para o estado de um objeto VMSS local chamado LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="75d57-109">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object named LocalVMSS.</span></span>

## <span data-ttu-id="75d57-110">OS</span><span class="sxs-lookup"><span data-stu-id="75d57-110">PARAMETERS</span></span>

### <span data-ttu-id="75d57-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d57-111">-DefaultProfile</span></span>
<span data-ttu-id="75d57-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75d57-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75d57-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d57-113">-ResourceGroupName</span></span>
<span data-ttu-id="75d57-114">Especifica o nome do grupo de recursos ao qual o VMSS pertence.</span><span class="sxs-lookup"><span data-stu-id="75d57-114">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="75d57-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="75d57-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="75d57-116">Especifica um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="75d57-116">Specifies a local VMSS object.</span></span>
<span data-ttu-id="75d57-117">Para obter um objeto VMSS, use o cmdlet Get-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="75d57-117">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="75d57-118">Esse objeto da máquina virtual contém o estado atualizado para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="75d57-118">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75d57-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="75d57-119">-VMScaleSetName</span></span>
<span data-ttu-id="75d57-120">Especifica o nome do VMSS que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="75d57-120">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="75d57-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75d57-121">-Confirm</span></span>
<span data-ttu-id="75d57-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75d57-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d57-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75d57-123">-WhatIf</span></span>
<span data-ttu-id="75d57-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75d57-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="75d57-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75d57-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d57-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d57-126">CommonParameters</span></span>
<span data-ttu-id="75d57-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75d57-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d57-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75d57-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d57-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75d57-129">INPUTS</span></span>

## <span data-ttu-id="75d57-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75d57-130">OUTPUTS</span></span>

## <span data-ttu-id="75d57-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75d57-131">NOTES</span></span>

## <span data-ttu-id="75d57-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75d57-132">RELATED LINKS</span></span>

[<span data-ttu-id="75d57-133">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="75d57-133">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="75d57-134">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="75d57-134">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="75d57-135">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="75d57-135">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="75d57-136">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="75d57-136">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="75d57-137">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="75d57-137">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="75d57-138">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="75d57-138">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="75d57-139">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="75d57-139">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


