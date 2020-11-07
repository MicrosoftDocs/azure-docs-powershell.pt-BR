---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 1b8f9b7843cccf2475e17e1c5d8866972b5b9ee4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955044"
---
# <span data-ttu-id="09bbb-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="09bbb-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="09bbb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="09bbb-103">Remove uma configuração de interface de rede de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="09bbb-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="09bbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09bbb-104">SYNTAX</span></span>

### <span data-ttu-id="09bbb-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09bbb-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09bbb-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09bbb-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09bbb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09bbb-107">DESCRIPTION</span></span>
<span data-ttu-id="09bbb-108">O cmdlet **Remove-AzVmssNetworkInterfaceConfiguration** remove uma configuração de interface de rede de um conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="09bbb-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="09bbb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09bbb-109">EXAMPLES</span></span>

### <span data-ttu-id="09bbb-110">Exemplo 1: remover uma configuração de interface</span><span class="sxs-lookup"><span data-stu-id="09bbb-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="09bbb-111">O primeiro comando obtém um VMSS usando o cmdlet Get-AzVmss e, em seguida, armazena-o na variável $VMSS.</span><span class="sxs-lookup"><span data-stu-id="09bbb-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="09bbb-112">O segundo comando Remove a configuração de interface de rede chamada ContosoVmssInterface02 do conjunto em $VMSS.</span><span class="sxs-lookup"><span data-stu-id="09bbb-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="09bbb-113">OS</span><span class="sxs-lookup"><span data-stu-id="09bbb-113">PARAMETERS</span></span>

### <span data-ttu-id="09bbb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09bbb-114">-DefaultProfile</span></span>
<span data-ttu-id="09bbb-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09bbb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09bbb-116">-ID</span><span class="sxs-lookup"><span data-stu-id="09bbb-116">-Id</span></span>
<span data-ttu-id="09bbb-117">Especifica a ID da configuração da interface de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="09bbb-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09bbb-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="09bbb-118">-Name</span></span>
<span data-ttu-id="09bbb-119">Especifica o nome da configuração da interface de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="09bbb-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="09bbb-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="09bbb-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="09bbb-121">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="09bbb-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="09bbb-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="09bbb-122">-Confirm</span></span>
<span data-ttu-id="09bbb-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09bbb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09bbb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09bbb-124">-WhatIf</span></span>
<span data-ttu-id="09bbb-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09bbb-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09bbb-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09bbb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09bbb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09bbb-127">CommonParameters</span></span>
<span data-ttu-id="09bbb-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09bbb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09bbb-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09bbb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09bbb-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09bbb-130">INPUTS</span></span>

### <span data-ttu-id="09bbb-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="09bbb-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="09bbb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="09bbb-132">System.String</span></span>

## <span data-ttu-id="09bbb-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09bbb-133">OUTPUTS</span></span>

### <span data-ttu-id="09bbb-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="09bbb-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="09bbb-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09bbb-135">NOTES</span></span>

## <span data-ttu-id="09bbb-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09bbb-136">RELATED LINKS</span></span>

[<span data-ttu-id="09bbb-137">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="09bbb-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="09bbb-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="09bbb-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


