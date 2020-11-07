---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextensionstatus
schema: 2.0.0
ms.openlocfilehash: b6ec9918657c191e31e10c04b799603654d39d56
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785272"
---
# <span data-ttu-id="4f5da-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="4f5da-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="4f5da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f5da-102">SYNOPSIS</span></span>
<span data-ttu-id="4f5da-103">Obtém o status do manipulador de extensão DSC para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4f5da-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f5da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f5da-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f5da-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f5da-105">DESCRIPTION</span></span>
<span data-ttu-id="4f5da-106">O cmdlet **Get-AzureRmVMDscExtensionStatus** Obtém o status do manipulador de extensão de configuração de estado desejado (DSC) de uma máquina virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4f5da-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="4f5da-107">Quando uma configuração é aplicada, esse cmdlet produz a saída consistente com o cmdlet Start-DscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4f5da-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="4f5da-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f5da-108">EXAMPLES</span></span>

### <span data-ttu-id="4f5da-109">1:</span><span class="sxs-lookup"><span data-stu-id="4f5da-109">1:</span></span>
```

```

## <span data-ttu-id="4f5da-110">OS</span><span class="sxs-lookup"><span data-stu-id="4f5da-110">PARAMETERS</span></span>

### <span data-ttu-id="4f5da-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f5da-111">-DefaultProfile</span></span>
<span data-ttu-id="4f5da-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4f5da-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f5da-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f5da-113">-Name</span></span>
<span data-ttu-id="4f5da-114">Especifica o nome do recurso do Gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="4f5da-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="4f5da-115">O cmdlet Set-AzureRmVMDscExtension define esse nome como Microsoft. PowerShell. DSC, que é o mesmo valor que é usado pelo **Get-AzureRmVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="4f5da-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="4f5da-116">Especifique esse parâmetro somente se você tiver alterado o nome padrão no cmdlet Set ou usado um nome de recurso diferente em um modelo do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="4f5da-116">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="4f5da-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f5da-117">-ResourceGroupName</span></span>
<span data-ttu-id="4f5da-118">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4f5da-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4f5da-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="4f5da-119">-VMName</span></span>
<span data-ttu-id="4f5da-120">Especifica o nome de uma máquina virtual para a qual esse cmdlet obtém o status da extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="4f5da-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="4f5da-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f5da-121">CommonParameters</span></span>
<span data-ttu-id="4f5da-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f5da-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f5da-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f5da-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f5da-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f5da-124">INPUTS</span></span>

### <span data-ttu-id="4f5da-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4f5da-125">None</span></span>
<span data-ttu-id="4f5da-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4f5da-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f5da-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f5da-127">OUTPUTS</span></span>

### <span data-ttu-id="4f5da-128">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="4f5da-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="4f5da-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f5da-129">NOTES</span></span>

## <span data-ttu-id="4f5da-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f5da-130">RELATED LINKS</span></span>

[<span data-ttu-id="4f5da-131">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4f5da-131">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


