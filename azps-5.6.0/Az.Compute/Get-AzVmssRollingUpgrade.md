---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: e87c307592f4487de239245ef06a70ea084ef916
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886090"
---
# <span data-ttu-id="4d4f4-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="4d4f4-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="4d4f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d4f4-102">SYNOPSIS</span></span>
<span data-ttu-id="4d4f4-103">Mostra o status da atualização de rolagem do conjunto de escalas de máquina virtual mais recente.</span><span class="sxs-lookup"><span data-stu-id="4d4f4-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="4d4f4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4d4f4-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d4f4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4d4f4-105">DESCRIPTION</span></span>
<span data-ttu-id="4d4f4-106">Mostra o status da atualização de rolagem do conjunto de escalas de máquina virtual mais recente.</span><span class="sxs-lookup"><span data-stu-id="4d4f4-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="4d4f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d4f4-107">EXAMPLES</span></span>

### <span data-ttu-id="4d4f4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4d4f4-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="4d4f4-109">Este comando mostra o status da atualização mais recente do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="4d4f4-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="4d4f4-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4d4f4-110">PARAMETERS</span></span>

### <span data-ttu-id="4d4f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d4f4-111">-DefaultProfile</span></span>
<span data-ttu-id="4d4f4-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4d4f4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d4f4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d4f4-113">-ResourceGroupName</span></span>
<span data-ttu-id="4d4f4-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d4f4-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="4d4f4-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4d4f4-115">-VMScaleSetName</span></span>
<span data-ttu-id="4d4f4-116">O nome do conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="4d4f4-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="4d4f4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d4f4-117">CommonParameters</span></span>
<span data-ttu-id="4d4f4-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d4f4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d4f4-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d4f4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d4f4-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d4f4-120">INPUTS</span></span>

### <span data-ttu-id="4d4f4-121">System.String</span><span class="sxs-lookup"><span data-stu-id="4d4f4-121">System.String</span></span>

## <span data-ttu-id="4d4f4-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4d4f4-122">OUTPUTS</span></span>

### <span data-ttu-id="4d4f4-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="4d4f4-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="4d4f4-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="4d4f4-124">NOTES</span></span>

## <span data-ttu-id="4d4f4-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d4f4-125">RELATED LINKS</span></span>
