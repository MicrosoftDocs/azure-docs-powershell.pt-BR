---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: 4b17cbb748a9841e0c22f4b8d8742562876fb9db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127101"
---
# <span data-ttu-id="d8797-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="d8797-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="d8797-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8797-102">SYNOPSIS</span></span>
<span data-ttu-id="d8797-103">Obtém as SKUs disponíveis para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="d8797-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="d8797-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8797-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8797-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8797-105">DESCRIPTION</span></span>
<span data-ttu-id="d8797-106">O cmdlet **Get-AzVmssSku** obtém as SKUs disponíveis para o VMSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="d8797-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d8797-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d8797-107">EXAMPLES</span></span>

### <span data-ttu-id="d8797-108">Exemplo 1: Obter todas as SKUs disponíveis no VMSS</span><span class="sxs-lookup"><span data-stu-id="d8797-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="d8797-109">Esse comando obtém todas as SKUs disponíveis do VMSS chamado ContosoVMSS que pertence ao grupo de recursos chamado ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="d8797-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="d8797-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8797-110">PARAMETERS</span></span>

### <span data-ttu-id="d8797-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8797-111">-DefaultProfile</span></span>
<span data-ttu-id="d8797-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d8797-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8797-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8797-113">-ResourceGroupName</span></span>
<span data-ttu-id="d8797-114">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="d8797-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="d8797-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d8797-115">-VMScaleSetName</span></span>
<span data-ttu-id="d8797-116">Especimos o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="d8797-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="d8797-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8797-117">CommonParameters</span></span>
<span data-ttu-id="d8797-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8797-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8797-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8797-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8797-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="d8797-120">INPUTS</span></span>

### <span data-ttu-id="d8797-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d8797-121">System.String</span></span>

## <span data-ttu-id="d8797-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="d8797-122">OUTPUTS</span></span>

### <span data-ttu-id="d8797-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="d8797-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="d8797-124">Notas</span><span class="sxs-lookup"><span data-stu-id="d8797-124">NOTES</span></span>

## <span data-ttu-id="d8797-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8797-125">RELATED LINKS</span></span>

[<span data-ttu-id="d8797-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d8797-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


