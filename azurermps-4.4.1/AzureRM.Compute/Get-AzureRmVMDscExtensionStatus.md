---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 0a14bf4f2c8a4b686f222079cadaec1744e41d08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432648"
---
# <span data-ttu-id="7bf5e-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="7bf5e-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="7bf5e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bf5e-102">SYNOPSIS</span></span>
<span data-ttu-id="7bf5e-103">Obtém o status do manipulador de extensão DSC para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bf5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bf5e-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bf5e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7bf5e-105">DESCRIPTION</span></span>
<span data-ttu-id="7bf5e-106">O cmdlet **Get-AzureRmVMDscExtensionStatus** Obtém o status do manipulador de extensão de configuração de estado desejado (DSC) de uma máquina virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="7bf5e-107">Quando uma configuração é aplicada, esse cmdlet produz a saída consistente com o cmdlet Start-DscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="7bf5e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bf5e-108">EXAMPLES</span></span>

## <span data-ttu-id="7bf5e-109">OS</span><span class="sxs-lookup"><span data-stu-id="7bf5e-109">PARAMETERS</span></span>

### <span data-ttu-id="7bf5e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bf5e-110">-DefaultProfile</span></span>
<span data-ttu-id="7bf5e-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bf5e-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="7bf5e-112">-Name</span></span>
<span data-ttu-id="7bf5e-113">Especifica o nome do recurso do Gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-113">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="7bf5e-114">O cmdlet Set-AzureRmVMDscExtension define esse nome como Microsoft. PowerShell. DSC, que é o mesmo valor que é usado pelo **Get-AzureRmVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-114">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="7bf5e-115">Especifique esse parâmetro somente se você tiver alterado o nome padrão no cmdlet Set ou usado um nome de recurso diferente em um modelo do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-115">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bf5e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bf5e-116">-ResourceGroupName</span></span>
<span data-ttu-id="7bf5e-117">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7bf5e-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="7bf5e-118">-VMName</span></span>
<span data-ttu-id="7bf5e-119">Especifica o nome de uma máquina virtual para a qual esse cmdlet obtém o status da extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-119">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="7bf5e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bf5e-120">CommonParameters</span></span>
<span data-ttu-id="7bf5e-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bf5e-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bf5e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bf5e-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7bf5e-123">INPUTS</span></span>

## <span data-ttu-id="7bf5e-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7bf5e-124">OUTPUTS</span></span>

## <span data-ttu-id="7bf5e-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7bf5e-125">NOTES</span></span>

## <span data-ttu-id="7bf5e-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bf5e-126">RELATED LINKS</span></span>

[<span data-ttu-id="7bf5e-127">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="7bf5e-127">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)

