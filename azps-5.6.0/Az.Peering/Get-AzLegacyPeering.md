---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: 2f1bdfd317a5578c5ce3a023f1c3cd0151026b80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890181"
---
# <span data-ttu-id="a7340-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="a7340-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="a7340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7340-102">SYNOPSIS</span></span>
<span data-ttu-id="a7340-103">Usado para converter recursos de peering herdados em recursos do Azure Resource Management (ARM).</span><span class="sxs-lookup"><span data-stu-id="a7340-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="a7340-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a7340-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7340-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a7340-105">DESCRIPTION</span></span>
<span data-ttu-id="a7340-106">O comando é usado para exibir recursos de peering herdados que você deve convertê-los em Recursos de Gerenciamento de Recursos do Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="a7340-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="a7340-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7340-107">EXAMPLES</span></span>

### <span data-ttu-id="a7340-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7340-108">Example 1</span></span>
```powershell
PS C:> Get-AzLegacyPeering -PeeringLocation "Seattle" -Kind Direct

Name                       :
Sku                        : Basic_Direct_Free
Kind                       : Direct
PeeringLocation            : Seattle
UseForPeeringService       : False
PeerAsn.Id                 :
Connection                 : ------------------------
PeeringDBFacilityId        : 71
SessionPrefixIPv4          : 173.205.50.236/30
PeerSessionIPv4Address     : 173.205.50.237
MicrosoftIPv4Address       : 173.205.50.238
SessionStateV4             : Established
MaxPrefixesAdvertisedV4    : 20000
SessionPrefixIPv6          : 2001:668:0:3:ffff:0:adcd:32ec/126
PeerSessionIPv6Address     : 2001:668:0:3:ffff:0:adcd:32ed
MicrosoftIPv6Address       : 2001:668:0:3:ffff:0:adcd:32ee
SessionStateV6             : Established
MaxPrefixesAdvertisedV6    : 2000
ConnectionState            : Active
BandwidthInMbps            : 0
ProvisionedBandwidthInMbps : 20000
ProvisioningState          : Succeeded
```

<span data-ttu-id="a7340-109">Obtém a paração herdda para Seattle</span><span class="sxs-lookup"><span data-stu-id="a7340-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="a7340-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a7340-110">PARAMETERS</span></span>

### <span data-ttu-id="a7340-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7340-111">-DefaultProfile</span></span>
<span data-ttu-id="a7340-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7340-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7340-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="a7340-113">-Kind</span></span>
<span data-ttu-id="a7340-114">Mostra todo o recurso Peering por Tipo.</span><span class="sxs-lookup"><span data-stu-id="a7340-114">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7340-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="a7340-115">-PeeringLocation</span></span>
<span data-ttu-id="a7340-116">Mostra todo o recurso Peering por Tipo.</span><span class="sxs-lookup"><span data-stu-id="a7340-116">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7340-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7340-117">CommonParameters</span></span>
<span data-ttu-id="a7340-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7340-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7340-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7340-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7340-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7340-120">INPUTS</span></span>

### <span data-ttu-id="a7340-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a7340-121">None</span></span>

## <span data-ttu-id="a7340-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a7340-122">OUTPUTS</span></span>

### <span data-ttu-id="a7340-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="a7340-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="a7340-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="a7340-124">NOTES</span></span>

## <span data-ttu-id="a7340-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7340-125">RELATED LINKS</span></span>
