---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: ae7c7bdd41f21c3f9263a8ea65aab722512543f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890794"
---
# <span data-ttu-id="775ae-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="775ae-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="775ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="775ae-102">SYNOPSIS</span></span>
<span data-ttu-id="775ae-103">Retorne os tipos de ponto de extremidade particular disponíveis no local.</span><span class="sxs-lookup"><span data-stu-id="775ae-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="775ae-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="775ae-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="775ae-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="775ae-105">DESCRIPTION</span></span>
<span data-ttu-id="775ae-106">O cmdlet **Get-AzAvailablePrivateEndpointType** retorna todos os tipos de ponto de extremidade particular disponíveis no local.</span><span class="sxs-lookup"><span data-stu-id="775ae-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="775ae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="775ae-107">EXAMPLES</span></span>

### <span data-ttu-id="775ae-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="775ae-108">Example 1</span></span>
```powershell
Get-AzAvailablePrivateEndpointType -Location eastus

[
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename1",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Sql/servers"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename2",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Storage/accounts"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename3",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Cosmos/cosmosDbAccounts"
  }
]
```

<span data-ttu-id="775ae-109">Este exemplo retorna todos os tipos de ponto de extremidade particular disponíveis no local.</span><span class="sxs-lookup"><span data-stu-id="775ae-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="775ae-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="775ae-110">PARAMETERS</span></span>

### <span data-ttu-id="775ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="775ae-111">-DefaultProfile</span></span>
<span data-ttu-id="775ae-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="775ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="775ae-113">-Location</span><span class="sxs-lookup"><span data-stu-id="775ae-113">-Location</span></span>
<span data-ttu-id="775ae-114">O local.</span><span class="sxs-lookup"><span data-stu-id="775ae-114">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="775ae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="775ae-115">-ResourceGroupName</span></span>
<span data-ttu-id="775ae-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="775ae-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="775ae-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="775ae-117">CommonParameters</span></span>
<span data-ttu-id="775ae-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="775ae-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="775ae-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="775ae-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="775ae-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="775ae-120">INPUTS</span></span>

### <span data-ttu-id="775ae-121">System.String</span><span class="sxs-lookup"><span data-stu-id="775ae-121">System.String</span></span>

## <span data-ttu-id="775ae-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="775ae-122">OUTPUTS</span></span>

### <span data-ttu-id="775ae-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="775ae-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="775ae-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="775ae-124">NOTES</span></span>

## <span data-ttu-id="775ae-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="775ae-125">RELATED LINKS</span></span>
