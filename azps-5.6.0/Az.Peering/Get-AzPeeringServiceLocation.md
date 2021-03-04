---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 84cc6f2e8e51de6176b4ab8a04296aab8516a967
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890162"
---
# <span data-ttu-id="cacb0-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="cacb0-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="cacb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cacb0-102">SYNOPSIS</span></span>
<span data-ttu-id="cacb0-103">Obtém uma lista de locais de serviço de paração oferecidos pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cacb0-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="cacb0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cacb0-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cacb0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cacb0-105">DESCRIPTION</span></span>
<span data-ttu-id="cacb0-106">Listar locais de peering.</span><span class="sxs-lookup"><span data-stu-id="cacb0-106">List peering locations.</span></span>

## <span data-ttu-id="cacb0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cacb0-107">EXAMPLES</span></span>

### <span data-ttu-id="cacb0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cacb0-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="cacb0-109">Recupera os locais de paração para Washington.</span><span class="sxs-lookup"><span data-stu-id="cacb0-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="cacb0-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cacb0-110">Example 2</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States"

Country     : United States
State       : Alabama
AzureRegion : East US
Name        : Alabama
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

Country     : United States
State       : Arizona
AzureRegion : West US
Name        : Arizona
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

...
```

<span data-ttu-id="cacb0-111">Recupera os locais de paração para Washington.</span><span class="sxs-lookup"><span data-stu-id="cacb0-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="cacb0-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cacb0-112">PARAMETERS</span></span>

### <span data-ttu-id="cacb0-113">-Country</span><span class="sxs-lookup"><span data-stu-id="cacb0-113">-Country</span></span>
<span data-ttu-id="cacb0-114">O filtro de país</span><span class="sxs-lookup"><span data-stu-id="cacb0-114">The country filter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cacb0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cacb0-115">-DefaultProfile</span></span>
<span data-ttu-id="cacb0-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cacb0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cacb0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cacb0-117">CommonParameters</span></span>
<span data-ttu-id="cacb0-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cacb0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cacb0-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cacb0-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cacb0-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cacb0-120">INPUTS</span></span>

### <span data-ttu-id="cacb0-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cacb0-121">None</span></span>

## <span data-ttu-id="cacb0-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cacb0-122">OUTPUTS</span></span>

### <span data-ttu-id="cacb0-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="cacb0-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="cacb0-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="cacb0-124">NOTES</span></span>

## <span data-ttu-id="cacb0-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cacb0-125">RELATED LINKS</span></span>
