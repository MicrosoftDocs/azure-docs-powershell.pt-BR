---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: a7696ee9738a885d3edea1eb8a3d2f9f7cea8510
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601330"
---
# <span data-ttu-id="83500-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="83500-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="83500-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83500-102">SYNOPSIS</span></span>
<span data-ttu-id="83500-103">Obtém os SKUs disponíveis para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="83500-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="83500-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83500-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83500-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="83500-105">DESCRIPTION</span></span>
<span data-ttu-id="83500-106">O cmdlet **Get-AzVmssSku** Obtém os SKUs disponíveis para o conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="83500-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="83500-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83500-107">EXAMPLES</span></span>

### <span data-ttu-id="83500-108">Exemplo 1: obter todas as SKUs disponíveis do VMSS</span><span class="sxs-lookup"><span data-stu-id="83500-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="83500-109">Esse comando obtém todas as SKUs disponíveis do VMSS chamado ContosoVMSS que pertence ao grupo de recursos chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="83500-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="83500-110">OS</span><span class="sxs-lookup"><span data-stu-id="83500-110">PARAMETERS</span></span>

### <span data-ttu-id="83500-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83500-111">-DefaultProfile</span></span>
<span data-ttu-id="83500-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="83500-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83500-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83500-113">-ResourceGroupName</span></span>
<span data-ttu-id="83500-114">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="83500-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="83500-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="83500-115">-VMScaleSetName</span></span>
<span data-ttu-id="83500-116">Especifica o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="83500-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="83500-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83500-117">CommonParameters</span></span>
<span data-ttu-id="83500-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83500-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83500-119">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83500-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83500-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="83500-120">INPUTS</span></span>

### <span data-ttu-id="83500-121">System. String</span><span class="sxs-lookup"><span data-stu-id="83500-121">System.String</span></span>

## <span data-ttu-id="83500-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="83500-122">OUTPUTS</span></span>

### <span data-ttu-id="83500-123">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="83500-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="83500-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="83500-124">NOTES</span></span>

## <span data-ttu-id="83500-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83500-125">RELATED LINKS</span></span>

[<span data-ttu-id="83500-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="83500-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


