---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: b89bf343c1737080867bbe5e8cb5397fd52f6a4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885486"
---
# <span data-ttu-id="b26f0-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="b26f0-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="b26f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b26f0-102">SYNOPSIS</span></span>
<span data-ttu-id="b26f0-103">Obtém as SKUs disponíveis para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="b26f0-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="b26f0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b26f0-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b26f0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b26f0-105">DESCRIPTION</span></span>
<span data-ttu-id="b26f0-106">O cmdlet **Get-AzVmssSku** obtém as SKUs disponíveis para o Conjunto de Escala de Máquina Virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b26f0-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b26f0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b26f0-107">EXAMPLES</span></span>

### <span data-ttu-id="b26f0-108">Exemplo 1: Obter todos os SKUs disponíveis no VMSS</span><span class="sxs-lookup"><span data-stu-id="b26f0-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="b26f0-109">Este comando obtém todos os SKUs disponíveis do VMSS chamado ContosoVMSS que pertence ao grupo de recursos chamado ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="b26f0-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="b26f0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b26f0-110">PARAMETERS</span></span>

### <span data-ttu-id="b26f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b26f0-111">-DefaultProfile</span></span>
<span data-ttu-id="b26f0-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b26f0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b26f0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b26f0-113">-ResourceGroupName</span></span>
<span data-ttu-id="b26f0-114">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="b26f0-114">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b26f0-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b26f0-115">-VMScaleSetName</span></span>
<span data-ttu-id="b26f0-116">Especiem o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="b26f0-116">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b26f0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b26f0-117">CommonParameters</span></span>
<span data-ttu-id="b26f0-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b26f0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b26f0-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b26f0-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b26f0-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b26f0-120">INPUTS</span></span>

### <span data-ttu-id="b26f0-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b26f0-121">System.String</span></span>

## <span data-ttu-id="b26f0-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b26f0-122">OUTPUTS</span></span>

### <span data-ttu-id="b26f0-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="b26f0-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="b26f0-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="b26f0-124">NOTES</span></span>

## <span data-ttu-id="b26f0-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b26f0-125">RELATED LINKS</span></span>

[<span data-ttu-id="b26f0-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b26f0-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


