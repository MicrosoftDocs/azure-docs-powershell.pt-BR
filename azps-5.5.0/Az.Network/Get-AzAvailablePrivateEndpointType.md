---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: 1ca9e604a1371d83fdedd2986534fa8926b6286b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113527"
---
# <span data-ttu-id="331ca-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="331ca-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="331ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="331ca-102">SYNOPSIS</span></span>
<span data-ttu-id="331ca-103">Retorne os tipos de ponto de extremidade particular disponíveis no local.</span><span class="sxs-lookup"><span data-stu-id="331ca-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="331ca-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="331ca-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="331ca-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="331ca-105">DESCRIPTION</span></span>
<span data-ttu-id="331ca-106">O cmdlet **Get-AzAvailablePrivateEndpointType** retorna todos os tipos de ponto de extremidade particular disponíveis no local.</span><span class="sxs-lookup"><span data-stu-id="331ca-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="331ca-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="331ca-107">EXAMPLES</span></span>

### <span data-ttu-id="331ca-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="331ca-108">Example 1</span></span>
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

<span data-ttu-id="331ca-109">Este exemplo retorna todos os tipos de ponto de extremidade particular disponíveis no local.</span><span class="sxs-lookup"><span data-stu-id="331ca-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="331ca-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="331ca-110">PARAMETERS</span></span>

### <span data-ttu-id="331ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="331ca-111">-DefaultProfile</span></span>
<span data-ttu-id="331ca-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="331ca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="331ca-113">-Local</span><span class="sxs-lookup"><span data-stu-id="331ca-113">-Location</span></span>
<span data-ttu-id="331ca-114">O local.</span><span class="sxs-lookup"><span data-stu-id="331ca-114">The location.</span></span>

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

### <span data-ttu-id="331ca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="331ca-115">-ResourceGroupName</span></span>
<span data-ttu-id="331ca-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="331ca-116">The resource group name.</span></span>

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

### <span data-ttu-id="331ca-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="331ca-117">CommonParameters</span></span>
<span data-ttu-id="331ca-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="331ca-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="331ca-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="331ca-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="331ca-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="331ca-120">INPUTS</span></span>

### <span data-ttu-id="331ca-121">System.String</span><span class="sxs-lookup"><span data-stu-id="331ca-121">System.String</span></span>

## <span data-ttu-id="331ca-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="331ca-122">OUTPUTS</span></span>

### <span data-ttu-id="331ca-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="331ca-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="331ca-124">Notas</span><span class="sxs-lookup"><span data-stu-id="331ca-124">NOTES</span></span>

## <span data-ttu-id="331ca-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="331ca-125">RELATED LINKS</span></span>
