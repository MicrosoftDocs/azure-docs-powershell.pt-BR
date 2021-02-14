---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 1b8f9b7843cccf2475e17e1c5d8866972b5b9ee4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111090"
---
# <span data-ttu-id="72ea4-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="72ea4-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="72ea4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="72ea4-103">Remove uma configuração de interface de rede de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="72ea4-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="72ea4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72ea4-104">SYNTAX</span></span>

### <span data-ttu-id="72ea4-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="72ea4-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72ea4-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="72ea4-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72ea4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="72ea4-107">DESCRIPTION</span></span>
<span data-ttu-id="72ea4-108">O cmdlet **Remove-AzVmssNetworkInterfaceConfiguration** remove uma configuração de interface de rede de um VMSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="72ea4-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="72ea4-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="72ea4-109">EXAMPLES</span></span>

### <span data-ttu-id="72ea4-110">Exemplo 1: Remover uma configuração de interface</span><span class="sxs-lookup"><span data-stu-id="72ea4-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="72ea4-111">O primeiro comando obtém um VMSS usando o cmdlet Get-AzVmss e, em seguida, o armazena na variável $VMSS dados.</span><span class="sxs-lookup"><span data-stu-id="72ea4-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="72ea4-112">O segundo comando remove a configuração da interface de rede chamada ContosoVmssInterface02 do conjunto em $VMSS.</span><span class="sxs-lookup"><span data-stu-id="72ea4-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="72ea4-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72ea4-113">PARAMETERS</span></span>

### <span data-ttu-id="72ea4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ea4-114">-DefaultProfile</span></span>
<span data-ttu-id="72ea4-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="72ea4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72ea4-116">-ID</span><span class="sxs-lookup"><span data-stu-id="72ea4-116">-Id</span></span>
<span data-ttu-id="72ea4-117">Especifica a ID da configuração da interface de rede que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="72ea4-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="72ea4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="72ea4-118">-Name</span></span>
<span data-ttu-id="72ea4-119">Especifica o nome da configuração da interface de rede que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="72ea4-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="72ea4-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="72ea4-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="72ea4-121">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="72ea4-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="72ea4-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="72ea4-122">-Confirm</span></span>
<span data-ttu-id="72ea4-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72ea4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72ea4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72ea4-124">-WhatIf</span></span>
<span data-ttu-id="72ea4-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="72ea4-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72ea4-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="72ea4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72ea4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ea4-127">CommonParameters</span></span>
<span data-ttu-id="72ea4-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72ea4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ea4-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72ea4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ea4-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="72ea4-130">INPUTS</span></span>

### <span data-ttu-id="72ea4-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="72ea4-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="72ea4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="72ea4-132">System.String</span></span>

## <span data-ttu-id="72ea4-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="72ea4-133">OUTPUTS</span></span>

### <span data-ttu-id="72ea4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="72ea4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="72ea4-135">Notas</span><span class="sxs-lookup"><span data-stu-id="72ea4-135">NOTES</span></span>

## <span data-ttu-id="72ea4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72ea4-136">RELATED LINKS</span></span>

[<span data-ttu-id="72ea4-137">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="72ea4-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="72ea4-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="72ea4-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


