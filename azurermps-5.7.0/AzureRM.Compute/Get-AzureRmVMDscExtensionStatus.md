---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 7cb7f175cc15e7d4e0915b6af9ef6fe6bdfc74d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427631"
---
# <span data-ttu-id="e1a1a-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="e1a1a-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="e1a1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a1a-103">Obtém o status do manipulador de extensão DSC para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e1a1a-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1a1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1a1a-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1a1a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1a1a-105">DESCRIPTION</span></span>
<span data-ttu-id="e1a1a-106">O cmdlet **Get-AzureRmVMDscExtensionStatus** Obtém o status do manipulador de extensão de configuração de estado desejado (DSC) de uma máquina virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e1a1a-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="e1a1a-107">Quando uma configuração é aplicada, esse cmdlet produz a saída consistente com o cmdlet Start-DscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e1a1a-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="e1a1a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1a1a-108">EXAMPLES</span></span>

## <span data-ttu-id="e1a1a-109">OS</span><span class="sxs-lookup"><span data-stu-id="e1a1a-109">PARAMETERS</span></span>

### <span data-ttu-id="e1a1a-110">-Nome</span><span class="sxs-lookup"><span data-stu-id="e1a1a-110">-Name</span></span>
<span data-ttu-id="e1a1a-111">Especifica o nome do recurso do Gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="e1a1a-111">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="e1a1a-112">O cmdlet Set-AzureRmVMDscExtension define esse nome como Microsoft. PowerShell. DSC, que é o mesmo valor que é usado pelo **Get-AzureRmVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="e1a1a-112">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="e1a1a-113">Especifique esse parâmetro somente se você tiver alterado o nome padrão no cmdlet Set ou usado um nome de recurso diferente em um modelo do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="e1a1a-113">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a1a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1a1a-114">-ResourceGroupName</span></span>
<span data-ttu-id="e1a1a-115">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e1a1a-115">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a1a-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="e1a1a-116">-VMName</span></span>
<span data-ttu-id="e1a1a-117">Especifica o nome de uma máquina virtual para a qual esse cmdlet obtém o status da extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="e1a1a-117">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="e1a1a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a1a-118">CommonParameters</span></span>
<span data-ttu-id="e1a1a-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1a1a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a1a-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1a1a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a1a-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1a1a-121">INPUTS</span></span>

### <span data-ttu-id="e1a1a-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e1a1a-122">None</span></span>
<span data-ttu-id="e1a1a-123">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e1a1a-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1a1a-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1a1a-124">OUTPUTS</span></span>

## <span data-ttu-id="e1a1a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1a1a-125">NOTES</span></span>

## <span data-ttu-id="e1a1a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1a1a-126">RELATED LINKS</span></span>

[<span data-ttu-id="e1a1a-127">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e1a1a-127">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


