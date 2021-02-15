---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 11c5e3ff2d8ee548917de7a94b1a592ae4cce52b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114158"
---
# <span data-ttu-id="25c96-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="25c96-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="25c96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25c96-102">SYNOPSIS</span></span>
<span data-ttu-id="25c96-103">Obter um IpGroup do Azure</span><span class="sxs-lookup"><span data-stu-id="25c96-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="25c96-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25c96-104">SYNTAX</span></span>

### <span data-ttu-id="25c96-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="25c96-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25c96-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25c96-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25c96-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="25c96-107">DESCRIPTION</span></span>
<span data-ttu-id="25c96-108">O **cmdlet Get-AzIpGroup** obtém um Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="25c96-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="25c96-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="25c96-109">EXAMPLES</span></span>

### <span data-ttu-id="25c96-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="25c96-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="25c96-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="25c96-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="25c96-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25c96-112">PARAMETERS</span></span>

### <span data-ttu-id="25c96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25c96-113">-DefaultProfile</span></span>
<span data-ttu-id="25c96-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25c96-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25c96-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="25c96-115">-Name</span></span>
<span data-ttu-id="25c96-116">O nome do grupo ip.</span><span class="sxs-lookup"><span data-stu-id="25c96-116">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25c96-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25c96-117">-ResourceGroupName</span></span>
<span data-ttu-id="25c96-118">O nome do grupo de recursos do grupo ip.</span><span class="sxs-lookup"><span data-stu-id="25c96-118">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25c96-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25c96-119">-ResourceId</span></span>
<span data-ttu-id="25c96-120">ResourceId do grupo ip.</span><span class="sxs-lookup"><span data-stu-id="25c96-120">ResourceId of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25c96-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25c96-121">CommonParameters</span></span>
<span data-ttu-id="25c96-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25c96-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25c96-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25c96-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25c96-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="25c96-124">INPUTS</span></span>

### <span data-ttu-id="25c96-125">System.String</span><span class="sxs-lookup"><span data-stu-id="25c96-125">System.String</span></span>

## <span data-ttu-id="25c96-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="25c96-126">OUTPUTS</span></span>

### <span data-ttu-id="25c96-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="25c96-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="25c96-128">Notas</span><span class="sxs-lookup"><span data-stu-id="25c96-128">NOTES</span></span>

## <span data-ttu-id="25c96-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25c96-129">RELATED LINKS</span></span>
