---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: 9a2fcb87b05d4478ab7b3e3490feae92fd727ce7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772865"
---
# <span data-ttu-id="64555-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="64555-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="64555-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64555-102">SYNOPSIS</span></span>
<span data-ttu-id="64555-103">Usado para converter recursos de emparelhamento herdados para recursos de gerenciamento de recursos do Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="64555-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="64555-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64555-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64555-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64555-105">DESCRIPTION</span></span>
<span data-ttu-id="64555-106">O comando é usado para exibir recursos de emparelhamento herdados que você deseja converter em recursos de gerenciamento de recursos do Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="64555-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="64555-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64555-107">EXAMPLES</span></span>

### <span data-ttu-id="64555-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="64555-108">Example 1</span></span>
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

<span data-ttu-id="64555-109">Obtém o emparelhamento herdado para Seattle</span><span class="sxs-lookup"><span data-stu-id="64555-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="64555-110">OS</span><span class="sxs-lookup"><span data-stu-id="64555-110">PARAMETERS</span></span>

### <span data-ttu-id="64555-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64555-111">-DefaultProfile</span></span>
<span data-ttu-id="64555-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64555-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64555-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="64555-113">-Kind</span></span>
<span data-ttu-id="64555-114">Mostra todos os recursos de emparelhamento por tipo.</span><span class="sxs-lookup"><span data-stu-id="64555-114">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="64555-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="64555-115">-PeeringLocation</span></span>
<span data-ttu-id="64555-116">Mostra todos os recursos de emparelhamento por tipo.</span><span class="sxs-lookup"><span data-stu-id="64555-116">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="64555-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64555-117">CommonParameters</span></span>
<span data-ttu-id="64555-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64555-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64555-119">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64555-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64555-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64555-120">INPUTS</span></span>

### <span data-ttu-id="64555-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="64555-121">None</span></span>

## <span data-ttu-id="64555-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64555-122">OUTPUTS</span></span>

### <span data-ttu-id="64555-123">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="64555-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="64555-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64555-124">NOTES</span></span>

## <span data-ttu-id="64555-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64555-125">RELATED LINKS</span></span>
