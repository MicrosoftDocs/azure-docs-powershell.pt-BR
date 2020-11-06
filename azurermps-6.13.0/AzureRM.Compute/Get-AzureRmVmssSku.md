---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: c906d7b0b10197e934ace7f9c913ee36e02be7ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433305"
---
# <span data-ttu-id="475f4-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="475f4-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="475f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="475f4-102">SYNOPSIS</span></span>
<span data-ttu-id="475f4-103">Obtém os SKUs disponíveis para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="475f4-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="475f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="475f4-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="475f4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="475f4-105">DESCRIPTION</span></span>
<span data-ttu-id="475f4-106">O cmdlet **Get-AzureRmVmssSku** Obtém os SKUs disponíveis para o conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="475f4-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="475f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="475f4-107">EXAMPLES</span></span>

### <span data-ttu-id="475f4-108">Exemplo 1: obter todas as SKUs disponíveis do VMSS</span><span class="sxs-lookup"><span data-stu-id="475f4-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="475f4-109">Esse comando obtém todas as SKUs disponíveis do VMSS chamado ContosoVMSS que pertence ao grupo de recursos chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="475f4-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="475f4-110">OS</span><span class="sxs-lookup"><span data-stu-id="475f4-110">PARAMETERS</span></span>

### <span data-ttu-id="475f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475f4-111">-DefaultProfile</span></span>
<span data-ttu-id="475f4-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="475f4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="475f4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="475f4-113">-ResourceGroupName</span></span>
<span data-ttu-id="475f4-114">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="475f4-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="475f4-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="475f4-115">-VMScaleSetName</span></span>
<span data-ttu-id="475f4-116">Especifica o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="475f4-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="475f4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475f4-117">CommonParameters</span></span>
<span data-ttu-id="475f4-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="475f4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475f4-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="475f4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475f4-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="475f4-120">INPUTS</span></span>

### <span data-ttu-id="475f4-121">System. String</span><span class="sxs-lookup"><span data-stu-id="475f4-121">System.String</span></span>

## <span data-ttu-id="475f4-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="475f4-122">OUTPUTS</span></span>

### <span data-ttu-id="475f4-123">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="475f4-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="475f4-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="475f4-124">NOTES</span></span>

## <span data-ttu-id="475f4-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="475f4-125">RELATED LINKS</span></span>

[<span data-ttu-id="475f4-126">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="475f4-126">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


