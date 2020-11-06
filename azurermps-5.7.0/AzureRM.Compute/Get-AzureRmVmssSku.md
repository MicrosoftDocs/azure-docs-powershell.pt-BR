---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: c86bf549c0de3643aaba67143b7df78f6fce798c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427621"
---
# <span data-ttu-id="f2731-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="f2731-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="f2731-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2731-102">SYNOPSIS</span></span>
<span data-ttu-id="f2731-103">Obtém os SKUs disponíveis para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="f2731-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2731-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2731-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String> [<CommonParameters>]
```

## <span data-ttu-id="f2731-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2731-105">DESCRIPTION</span></span>
<span data-ttu-id="f2731-106">O cmdlet **Get-AzureRmVmssSku** Obtém os SKUs disponíveis para o conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f2731-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="f2731-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2731-107">EXAMPLES</span></span>

### <span data-ttu-id="f2731-108">Exemplo 1: obter todas as SKUs disponíveis do VMSS</span><span class="sxs-lookup"><span data-stu-id="f2731-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="f2731-109">Esse comando obtém todas as SKUs disponíveis do VMSS chamado ContosoVMSS que pertence ao grupo de recursos chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="f2731-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="f2731-110">OS</span><span class="sxs-lookup"><span data-stu-id="f2731-110">PARAMETERS</span></span>

### <span data-ttu-id="f2731-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2731-111">-ResourceGroupName</span></span>
<span data-ttu-id="f2731-112">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="f2731-112">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="f2731-113">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f2731-113">-VMScaleSetName</span></span>
<span data-ttu-id="f2731-114">Especifica o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="f2731-114">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="f2731-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2731-115">CommonParameters</span></span>
<span data-ttu-id="f2731-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2731-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2731-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2731-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2731-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2731-118">INPUTS</span></span>

### <span data-ttu-id="f2731-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f2731-119">None</span></span>
<span data-ttu-id="f2731-120">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f2731-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2731-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2731-121">OUTPUTS</span></span>

### <span data-ttu-id="f2731-122">Esse cmdlet não produz nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f2731-122">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="f2731-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2731-123">NOTES</span></span>

## <span data-ttu-id="f2731-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2731-124">RELATED LINKS</span></span>

[<span data-ttu-id="f2731-125">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f2731-125">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


