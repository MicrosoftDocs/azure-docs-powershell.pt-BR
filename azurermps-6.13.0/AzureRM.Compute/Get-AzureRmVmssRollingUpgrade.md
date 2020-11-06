---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: ef83792704e24102e8e837768ee5acae5abbe548
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426427"
---
# <span data-ttu-id="81d25-101">Get-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="81d25-101">Get-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="81d25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81d25-102">SYNOPSIS</span></span>
<span data-ttu-id="81d25-103">Mostra o status da atualização sem interrupção da configuração de escala da máquina virtual mais recente.</span><span class="sxs-lookup"><span data-stu-id="81d25-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81d25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81d25-104">SYNTAX</span></span>

```
Get-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81d25-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81d25-105">DESCRIPTION</span></span>
<span data-ttu-id="81d25-106">Mostra o status da atualização sem interrupção da configuração de escala da máquina virtual mais recente.</span><span class="sxs-lookup"><span data-stu-id="81d25-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="81d25-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81d25-107">EXAMPLES</span></span>

### <span data-ttu-id="81d25-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="81d25-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="81d25-109">Esse comando mostra o status da atualização sem interrupção mais recente do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="81d25-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="81d25-110">OS</span><span class="sxs-lookup"><span data-stu-id="81d25-110">PARAMETERS</span></span>

### <span data-ttu-id="81d25-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d25-111">-DefaultProfile</span></span>
<span data-ttu-id="81d25-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81d25-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81d25-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d25-113">-ResourceGroupName</span></span>
<span data-ttu-id="81d25-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="81d25-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="81d25-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="81d25-115">-VMScaleSetName</span></span>
<span data-ttu-id="81d25-116">O nome do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="81d25-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="81d25-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d25-117">CommonParameters</span></span>
<span data-ttu-id="81d25-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81d25-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d25-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81d25-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d25-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81d25-120">INPUTS</span></span>

### <span data-ttu-id="81d25-121">System. String</span><span class="sxs-lookup"><span data-stu-id="81d25-121">System.String</span></span>

## <span data-ttu-id="81d25-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81d25-122">OUTPUTS</span></span>

### <span data-ttu-id="81d25-123">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="81d25-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="81d25-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81d25-124">NOTES</span></span>

## <span data-ttu-id="81d25-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81d25-125">RELATED LINKS</span></span>
