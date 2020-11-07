---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsssku
schema: 2.0.0
ms.openlocfilehash: 307b9852f506368e1e13c02fac4532dab4d2ddd2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785991"
---
# <span data-ttu-id="7954d-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="7954d-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="7954d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7954d-102">SYNOPSIS</span></span>
<span data-ttu-id="7954d-103">Obtém os SKUs disponíveis para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="7954d-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7954d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7954d-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7954d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7954d-105">DESCRIPTION</span></span>
<span data-ttu-id="7954d-106">O cmdlet **Get-AzureRmVmssSku** Obtém os SKUs disponíveis para o conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="7954d-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="7954d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7954d-107">EXAMPLES</span></span>

### <span data-ttu-id="7954d-108">Exemplo 1: obter todas as SKUs disponíveis do VMSS</span><span class="sxs-lookup"><span data-stu-id="7954d-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="7954d-109">Esse comando obtém todas as SKUs disponíveis do VMSS chamado ContosoVMSS que pertence ao grupo de recursos chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="7954d-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="7954d-110">OS</span><span class="sxs-lookup"><span data-stu-id="7954d-110">PARAMETERS</span></span>

### <span data-ttu-id="7954d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7954d-111">-DefaultProfile</span></span>
<span data-ttu-id="7954d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7954d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7954d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7954d-113">-ResourceGroupName</span></span>
<span data-ttu-id="7954d-114">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="7954d-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="7954d-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7954d-115">-VMScaleSetName</span></span>
<span data-ttu-id="7954d-116">Especifica o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="7954d-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="7954d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7954d-117">CommonParameters</span></span>
<span data-ttu-id="7954d-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7954d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7954d-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7954d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7954d-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7954d-120">INPUTS</span></span>

### <span data-ttu-id="7954d-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7954d-121">None</span></span>
<span data-ttu-id="7954d-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="7954d-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7954d-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7954d-123">OUTPUTS</span></span>

### <span data-ttu-id="7954d-124">Esse cmdlet não produz nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="7954d-124">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="7954d-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7954d-125">NOTES</span></span>

## <span data-ttu-id="7954d-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7954d-126">RELATED LINKS</span></span>

[<span data-ttu-id="7954d-127">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7954d-127">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


