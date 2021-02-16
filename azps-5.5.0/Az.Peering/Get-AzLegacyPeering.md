---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: e7b5ef8ef41c66cc3c19fd5ebdcfd53ddcc6f3a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113390"
---
# <span data-ttu-id="493d9-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="493d9-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="493d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="493d9-102">SYNOPSIS</span></span>
<span data-ttu-id="493d9-103">Usado para converter recursos de peering herdados em recursos arm (gerenciamento de recursos) do Azure.</span><span class="sxs-lookup"><span data-stu-id="493d9-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="493d9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="493d9-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="493d9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="493d9-105">DESCRIPTION</span></span>
<span data-ttu-id="493d9-106">O comando é usado para exibir recursos herdados de Peering, que você pode convertê-los em Recursos de Gerenciamento de Recursos do Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="493d9-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="493d9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="493d9-107">EXAMPLES</span></span>

### <span data-ttu-id="493d9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="493d9-108">Example 1</span></span>
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

<span data-ttu-id="493d9-109">Obtém o paramento herddo de Seattle</span><span class="sxs-lookup"><span data-stu-id="493d9-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="493d9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="493d9-110">PARAMETERS</span></span>

### <span data-ttu-id="493d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="493d9-111">-DefaultProfile</span></span>
<span data-ttu-id="493d9-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="493d9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="493d9-113">-Tipo</span><span class="sxs-lookup"><span data-stu-id="493d9-113">-Kind</span></span>
<span data-ttu-id="493d9-114">Mostra todos os recursos de Peering por Tipo.</span><span class="sxs-lookup"><span data-stu-id="493d9-114">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="493d9-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="493d9-115">-PeeringLocation</span></span>
<span data-ttu-id="493d9-116">Mostra todos os recursos de Peering por Tipo.</span><span class="sxs-lookup"><span data-stu-id="493d9-116">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="493d9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493d9-117">CommonParameters</span></span>
<span data-ttu-id="493d9-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="493d9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493d9-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="493d9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493d9-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="493d9-120">INPUTS</span></span>

### <span data-ttu-id="493d9-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="493d9-121">None</span></span>

## <span data-ttu-id="493d9-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="493d9-122">OUTPUTS</span></span>

### <span data-ttu-id="493d9-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="493d9-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="493d9-124">Notas</span><span class="sxs-lookup"><span data-stu-id="493d9-124">NOTES</span></span>

## <span data-ttu-id="493d9-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="493d9-125">RELATED LINKS</span></span>
