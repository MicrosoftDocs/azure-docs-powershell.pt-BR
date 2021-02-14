---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3ab0dc0acb02d2efa9f7da29dd096ad03f1eb57e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111145"
---
# <span data-ttu-id="38c44-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="38c44-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="38c44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38c44-102">SYNOPSIS</span></span>
<span data-ttu-id="38c44-103">Mostra o status da atualização em escala de máquina virtual mais recente.</span><span class="sxs-lookup"><span data-stu-id="38c44-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="38c44-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38c44-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38c44-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="38c44-105">DESCRIPTION</span></span>
<span data-ttu-id="38c44-106">Mostra o status da atualização em escala de máquina virtual mais recente.</span><span class="sxs-lookup"><span data-stu-id="38c44-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="38c44-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="38c44-107">EXAMPLES</span></span>

### <span data-ttu-id="38c44-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="38c44-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="38c44-109">Esse comando mostra o status da atualização em implantação mais recente do VMSS chamado VMSS01 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="38c44-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="38c44-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38c44-110">PARAMETERS</span></span>

### <span data-ttu-id="38c44-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c44-111">-DefaultProfile</span></span>
<span data-ttu-id="38c44-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="38c44-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38c44-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38c44-113">-ResourceGroupName</span></span>
<span data-ttu-id="38c44-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="38c44-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="38c44-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="38c44-115">-VMScaleSetName</span></span>
<span data-ttu-id="38c44-116">O nome do conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="38c44-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="38c44-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c44-117">CommonParameters</span></span>
<span data-ttu-id="38c44-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38c44-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c44-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38c44-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c44-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="38c44-120">INPUTS</span></span>

### <span data-ttu-id="38c44-121">System.String</span><span class="sxs-lookup"><span data-stu-id="38c44-121">System.String</span></span>

## <span data-ttu-id="38c44-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="38c44-122">OUTPUTS</span></span>

### <span data-ttu-id="38c44-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="38c44-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="38c44-124">Notas</span><span class="sxs-lookup"><span data-stu-id="38c44-124">NOTES</span></span>

## <span data-ttu-id="38c44-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38c44-125">RELATED LINKS</span></span>
