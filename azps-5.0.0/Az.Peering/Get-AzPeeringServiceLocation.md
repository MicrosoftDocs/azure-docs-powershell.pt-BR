---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 6f869cee7258c38e941ca8fbb7c8ac31b47171af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116372"
---
# <span data-ttu-id="7d563-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="7d563-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="7d563-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d563-102">SYNOPSIS</span></span>
<span data-ttu-id="7d563-103">Obtém uma lista de locais de serviço de emparelhamento oferecidos pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7d563-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="7d563-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d563-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d563-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d563-105">DESCRIPTION</span></span>
<span data-ttu-id="7d563-106">Locais de emparelhamento de lista.</span><span class="sxs-lookup"><span data-stu-id="7d563-106">List peering locations.</span></span>

## <span data-ttu-id="7d563-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d563-107">EXAMPLES</span></span>

### <span data-ttu-id="7d563-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7d563-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="7d563-109">Recupera os locais de emparelhamento para Washington.</span><span class="sxs-lookup"><span data-stu-id="7d563-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="7d563-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7d563-110">Example 2</span></span>
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

<span data-ttu-id="7d563-111">Recupera os locais de emparelhamento para Washington.</span><span class="sxs-lookup"><span data-stu-id="7d563-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="7d563-112">OS</span><span class="sxs-lookup"><span data-stu-id="7d563-112">PARAMETERS</span></span>

### <span data-ttu-id="7d563-113">-País</span><span class="sxs-lookup"><span data-stu-id="7d563-113">-Country</span></span>
<span data-ttu-id="7d563-114">O filtro país</span><span class="sxs-lookup"><span data-stu-id="7d563-114">The country filter</span></span>

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

### <span data-ttu-id="7d563-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d563-115">-DefaultProfile</span></span>
<span data-ttu-id="7d563-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d563-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d563-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d563-117">CommonParameters</span></span>
<span data-ttu-id="7d563-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d563-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d563-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d563-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d563-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d563-120">INPUTS</span></span>

### <span data-ttu-id="7d563-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7d563-121">None</span></span>

## <span data-ttu-id="7d563-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d563-122">OUTPUTS</span></span>

### <span data-ttu-id="7d563-123">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="7d563-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="7d563-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d563-124">NOTES</span></span>

## <span data-ttu-id="7d563-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d563-125">RELATED LINKS</span></span>
