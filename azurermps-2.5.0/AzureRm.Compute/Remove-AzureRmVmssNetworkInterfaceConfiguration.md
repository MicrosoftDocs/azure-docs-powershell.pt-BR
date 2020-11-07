---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
ms.openlocfilehash: 46058901188b99eb30d088e2ea784fdc0df8d782
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786330"
---
# <span data-ttu-id="dd01f-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd01f-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="dd01f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd01f-102">SYNOPSIS</span></span>
<span data-ttu-id="dd01f-103">Remove uma configuração de interface de rede de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="dd01f-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd01f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd01f-104">SYNTAX</span></span>

### <span data-ttu-id="dd01f-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd01f-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd01f-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd01f-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd01f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd01f-107">DESCRIPTION</span></span>
<span data-ttu-id="dd01f-108">O cmdlet **Remove-AzureRmVmssNetworkInterfaceConfiguration** remove uma configuração de interface de rede de um conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="dd01f-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="dd01f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd01f-109">EXAMPLES</span></span>

### <span data-ttu-id="dd01f-110">Exemplo 1: remover uma configuração de interface</span><span class="sxs-lookup"><span data-stu-id="dd01f-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="dd01f-111">O primeiro comando obtém um VMSS usando o cmdlet Get-AzureRmVmss e, em seguida, armazena-o na variável $VMSS.</span><span class="sxs-lookup"><span data-stu-id="dd01f-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="dd01f-112">O segundo comando Remove a configuração de interface de rede chamada ContosoVmssInterface02 do conjunto em $VMSS.</span><span class="sxs-lookup"><span data-stu-id="dd01f-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="dd01f-113">OS</span><span class="sxs-lookup"><span data-stu-id="dd01f-113">PARAMETERS</span></span>

### <span data-ttu-id="dd01f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd01f-114">-DefaultProfile</span></span>
<span data-ttu-id="dd01f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd01f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd01f-116">-ID</span><span class="sxs-lookup"><span data-stu-id="dd01f-116">-Id</span></span>
<span data-ttu-id="dd01f-117">Especifica a ID da configuração da interface de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="dd01f-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd01f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd01f-118">-Name</span></span>
<span data-ttu-id="dd01f-119">Especifica o nome da configuração da interface de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="dd01f-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dd01f-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dd01f-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="dd01f-121">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="dd01f-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="dd01f-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dd01f-122">-Confirm</span></span>
<span data-ttu-id="dd01f-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd01f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd01f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd01f-124">-WhatIf</span></span>
<span data-ttu-id="dd01f-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dd01f-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd01f-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd01f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd01f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd01f-127">CommonParameters</span></span>
<span data-ttu-id="dd01f-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd01f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd01f-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd01f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd01f-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd01f-130">INPUTS</span></span>

### <span data-ttu-id="dd01f-131">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dd01f-131">VirtualMachineScaleSet</span></span>
<span data-ttu-id="dd01f-132">O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="dd01f-132">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="dd01f-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd01f-133">OUTPUTS</span></span>

### <span data-ttu-id="dd01f-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dd01f-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="dd01f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd01f-135">NOTES</span></span>

## <span data-ttu-id="dd01f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd01f-136">RELATED LINKS</span></span>

[<span data-ttu-id="dd01f-137">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd01f-137">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="dd01f-138">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dd01f-138">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


