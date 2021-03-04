---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverrequiredforresources
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
ms.openlocfilehash: 9aa09de52a6b731fbf57b309fb605c0ba07325da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891653"
---
# <span data-ttu-id="4e73e-101">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="4e73e-101">Get-AzResourceMoverRequiredForResources</span></span>

## <span data-ttu-id="4e73e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e73e-102">SYNOPSIS</span></span>
<span data-ttu-id="4e73e-103">Lista dos recursos de movimentação para os quais um recurso arm é necessário.</span><span class="sxs-lookup"><span data-stu-id="4e73e-103">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="4e73e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4e73e-104">SYNTAX</span></span>

```
Get-AzResourceMoverRequiredForResources -MoveCollectionName <String> -ResourceGroupName <String>
 -SourceId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4e73e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4e73e-105">DESCRIPTION</span></span>
<span data-ttu-id="4e73e-106">Lista dos recursos de movimentação para os quais um recurso arm é necessário.</span><span class="sxs-lookup"><span data-stu-id="4e73e-106">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="4e73e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e73e-107">EXAMPLES</span></span>

### <span data-ttu-id="4e73e-108">Exemplo 1: obter uma lista de ARMIDs de recursos necessários que são necessários para serem adicionados, para adicionar o recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="4e73e-108">Example 1: Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>
```powershell
PS C:\> Get-AzResourceMoverRequiredForResources -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -SourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups"

/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="4e73e-109">Obter uma lista de ARMIDs de recursos necessários que são necessários para serem adicionados, para adicionar o recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="4e73e-109">Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>

## <span data-ttu-id="4e73e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4e73e-110">PARAMETERS</span></span>

### <span data-ttu-id="4e73e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e73e-111">-DefaultProfile</span></span>
<span data-ttu-id="4e73e-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e73e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e73e-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="4e73e-113">-MoveCollectionName</span></span>
<span data-ttu-id="4e73e-114">O nome da coleção Move.</span><span class="sxs-lookup"><span data-stu-id="4e73e-114">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e73e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e73e-115">-ResourceGroupName</span></span>
<span data-ttu-id="4e73e-116">O Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="4e73e-116">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e73e-117">-SourceId</span><span class="sxs-lookup"><span data-stu-id="4e73e-117">-SourceId</span></span>
<span data-ttu-id="4e73e-118">A sourceId para a qual a api é invocada.</span><span class="sxs-lookup"><span data-stu-id="4e73e-118">The sourceId for which the api is invoked.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e73e-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e73e-119">-SubscriptionId</span></span>
<span data-ttu-id="4e73e-120">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="4e73e-120">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e73e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e73e-121">CommonParameters</span></span>
<span data-ttu-id="4e73e-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e73e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e73e-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e73e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e73e-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e73e-124">INPUTS</span></span>

## <span data-ttu-id="4e73e-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4e73e-125">OUTPUTS</span></span>

### <span data-ttu-id="4e73e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4e73e-126">System.String</span></span>

## <span data-ttu-id="4e73e-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="4e73e-127">NOTES</span></span>

<span data-ttu-id="4e73e-128">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4e73e-128">ALIASES</span></span>

## <span data-ttu-id="4e73e-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e73e-129">RELATED LINKS</span></span>

