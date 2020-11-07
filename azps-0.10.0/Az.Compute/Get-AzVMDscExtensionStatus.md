---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: 3ae9827c6db5136b9327936a63ac0441dcf94ff1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777020"
---
# <span data-ttu-id="8ec75-101">Get-AzVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="8ec75-101">Get-AzVMDscExtensionStatus</span></span>

## <span data-ttu-id="8ec75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ec75-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec75-103">Obtém o status do manipulador de extensão DSC para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ec75-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

## <span data-ttu-id="8ec75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ec75-104">SYNTAX</span></span>

```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ec75-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ec75-105">DESCRIPTION</span></span>
<span data-ttu-id="8ec75-106">O cmdlet **Get-AzVMDscExtensionStatus** Obtém o status do manipulador de extensão de configuração de estado desejado (DSC) de uma máquina virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8ec75-106">The **Get-AzVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="8ec75-107">Quando uma configuração é aplicada, esse cmdlet produz a saída consistente com o cmdlet Start-DscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8ec75-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="8ec75-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ec75-108">EXAMPLES</span></span>

### <span data-ttu-id="8ec75-109">1:</span><span class="sxs-lookup"><span data-stu-id="8ec75-109">1:</span></span>
```

```

## <span data-ttu-id="8ec75-110">OS</span><span class="sxs-lookup"><span data-stu-id="8ec75-110">PARAMETERS</span></span>

### <span data-ttu-id="8ec75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec75-111">-DefaultProfile</span></span>
<span data-ttu-id="8ec75-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ec75-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ec75-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ec75-113">-Name</span></span>
<span data-ttu-id="8ec75-114">Especifica o nome do recurso do Gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="8ec75-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="8ec75-115">O cmdlet Set-AzVMDscExtension define esse nome como Microsoft. PowerShell. DSC, que é o mesmo valor que é usado pelo **Get-AzVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="8ec75-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtensionStatus**.</span></span>
<span data-ttu-id="8ec75-116">Especifique esse parâmetro somente se você tiver alterado o nome padrão no cmdlet Set ou usado um nome de recurso diferente em um modelo do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="8ec75-116">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="8ec75-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ec75-117">-ResourceGroupName</span></span>
<span data-ttu-id="8ec75-118">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ec75-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8ec75-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="8ec75-119">-VMName</span></span>
<span data-ttu-id="8ec75-120">Especifica o nome de uma máquina virtual para a qual esse cmdlet obtém o status da extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="8ec75-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="8ec75-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec75-121">CommonParameters</span></span>
<span data-ttu-id="8ec75-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ec75-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec75-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec75-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec75-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ec75-124">INPUTS</span></span>

### <span data-ttu-id="8ec75-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8ec75-125">None</span></span>
<span data-ttu-id="8ec75-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8ec75-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ec75-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ec75-127">OUTPUTS</span></span>

### <span data-ttu-id="8ec75-128">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="8ec75-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="8ec75-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ec75-129">NOTES</span></span>

## <span data-ttu-id="8ec75-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ec75-130">RELATED LINKS</span></span>

[<span data-ttu-id="8ec75-131">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8ec75-131">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


