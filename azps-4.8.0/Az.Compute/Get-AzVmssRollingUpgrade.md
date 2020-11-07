---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3ab0dc0acb02d2efa9f7da29dd096ad03f1eb57e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948126"
---
# <span data-ttu-id="c7528-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="c7528-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="c7528-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7528-102">SYNOPSIS</span></span>
<span data-ttu-id="c7528-103">Mostra o status da atualização sem interrupção da configuração de escala da máquina virtual mais recente.</span><span class="sxs-lookup"><span data-stu-id="c7528-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="c7528-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7528-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7528-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7528-105">DESCRIPTION</span></span>
<span data-ttu-id="c7528-106">Mostra o status da atualização sem interrupção da configuração de escala da máquina virtual mais recente.</span><span class="sxs-lookup"><span data-stu-id="c7528-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="c7528-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7528-107">EXAMPLES</span></span>

### <span data-ttu-id="c7528-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c7528-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="c7528-109">Esse comando mostra o status da atualização sem interrupção mais recente do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="c7528-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="c7528-110">OS</span><span class="sxs-lookup"><span data-stu-id="c7528-110">PARAMETERS</span></span>

### <span data-ttu-id="c7528-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7528-111">-DefaultProfile</span></span>
<span data-ttu-id="c7528-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7528-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7528-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7528-113">-ResourceGroupName</span></span>
<span data-ttu-id="c7528-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c7528-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="c7528-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c7528-115">-VMScaleSetName</span></span>
<span data-ttu-id="c7528-116">O nome do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="c7528-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="c7528-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7528-117">CommonParameters</span></span>
<span data-ttu-id="c7528-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7528-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7528-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7528-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7528-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7528-120">INPUTS</span></span>

### <span data-ttu-id="c7528-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c7528-121">System.String</span></span>

## <span data-ttu-id="c7528-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7528-122">OUTPUTS</span></span>

### <span data-ttu-id="c7528-123">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="c7528-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="c7528-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7528-124">NOTES</span></span>

## <span data-ttu-id="c7528-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7528-125">RELATED LINKS</span></span>
