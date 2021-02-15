---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 6f869cee7258c38e941ca8fbb7c8ac31b47171af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111511"
---
# <span data-ttu-id="33592-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="33592-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="33592-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33592-102">SYNOPSIS</span></span>
<span data-ttu-id="33592-103">Obtém uma lista de locais de serviço de pares oferecidos pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="33592-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="33592-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33592-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33592-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="33592-105">DESCRIPTION</span></span>
<span data-ttu-id="33592-106">Locais de paridade de lista.</span><span class="sxs-lookup"><span data-stu-id="33592-106">List peering locations.</span></span>

## <span data-ttu-id="33592-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="33592-107">EXAMPLES</span></span>

### <span data-ttu-id="33592-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="33592-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="33592-109">Recupera os locais de pares para Washington.</span><span class="sxs-lookup"><span data-stu-id="33592-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="33592-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="33592-110">Example 2</span></span>
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

<span data-ttu-id="33592-111">Recupera os locais de pares para Washington.</span><span class="sxs-lookup"><span data-stu-id="33592-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="33592-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33592-112">PARAMETERS</span></span>

### <span data-ttu-id="33592-113">-País/Região</span><span class="sxs-lookup"><span data-stu-id="33592-113">-Country</span></span>
<span data-ttu-id="33592-114">O filtro do país</span><span class="sxs-lookup"><span data-stu-id="33592-114">The country filter</span></span>

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

### <span data-ttu-id="33592-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33592-115">-DefaultProfile</span></span>
<span data-ttu-id="33592-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33592-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33592-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33592-117">CommonParameters</span></span>
<span data-ttu-id="33592-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33592-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33592-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33592-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33592-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="33592-120">INPUTS</span></span>

### <span data-ttu-id="33592-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="33592-121">None</span></span>

## <span data-ttu-id="33592-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="33592-122">OUTPUTS</span></span>

### <span data-ttu-id="33592-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="33592-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="33592-124">Notas</span><span class="sxs-lookup"><span data-stu-id="33592-124">NOTES</span></span>

## <span data-ttu-id="33592-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33592-125">RELATED LINKS</span></span>
