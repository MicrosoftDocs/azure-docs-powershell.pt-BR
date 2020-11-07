---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: d005f3f182109399f5a74b934959951dfb02c48e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776998"
---
# <span data-ttu-id="ba3b2-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="ba3b2-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="ba3b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba3b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ba3b2-103">Obtém os SKUs disponíveis para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="ba3b2-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="ba3b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba3b2-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba3b2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba3b2-105">DESCRIPTION</span></span>
<span data-ttu-id="ba3b2-106">O cmdlet **Get-AzVmssSku** Obtém os SKUs disponíveis para o conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ba3b2-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ba3b2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba3b2-107">EXAMPLES</span></span>

### <span data-ttu-id="ba3b2-108">Exemplo 1: obter todas as SKUs disponíveis do VMSS</span><span class="sxs-lookup"><span data-stu-id="ba3b2-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="ba3b2-109">Esse comando obtém todas as SKUs disponíveis do VMSS chamado ContosoVMSS que pertence ao grupo de recursos chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="ba3b2-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="ba3b2-110">OS</span><span class="sxs-lookup"><span data-stu-id="ba3b2-110">PARAMETERS</span></span>

### <span data-ttu-id="ba3b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba3b2-111">-DefaultProfile</span></span>
<span data-ttu-id="ba3b2-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba3b2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba3b2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba3b2-113">-ResourceGroupName</span></span>
<span data-ttu-id="ba3b2-114">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="ba3b2-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="ba3b2-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ba3b2-115">-VMScaleSetName</span></span>
<span data-ttu-id="ba3b2-116">Especifica o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="ba3b2-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="ba3b2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba3b2-117">CommonParameters</span></span>
<span data-ttu-id="ba3b2-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba3b2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba3b2-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba3b2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba3b2-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba3b2-120">INPUTS</span></span>

### <span data-ttu-id="ba3b2-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ba3b2-121">None</span></span>
<span data-ttu-id="ba3b2-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ba3b2-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba3b2-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba3b2-123">OUTPUTS</span></span>

### <span data-ttu-id="ba3b2-124">Esse cmdlet não produz nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ba3b2-124">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="ba3b2-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba3b2-125">NOTES</span></span>

## <span data-ttu-id="ba3b2-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba3b2-126">RELATED LINKS</span></span>

[<span data-ttu-id="ba3b2-127">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ba3b2-127">Get-AzVmss</span></span>](./Get-AzVmss.md)


