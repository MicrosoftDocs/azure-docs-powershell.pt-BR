---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: cfc25f735d2785a688f29fd3eb3064337b5c6e8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890160"
---
# <span data-ttu-id="2ea30-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="2ea30-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="2ea30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ea30-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea30-103">Obtém uma lista de provedores de serviços de paração em parceria com a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2ea30-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="2ea30-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2ea30-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ea30-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2ea30-105">DESCRIPTION</span></span>
<span data-ttu-id="2ea30-106">Listar provedores de serviços de paração</span><span class="sxs-lookup"><span data-stu-id="2ea30-106">List peering service providers</span></span>

## <span data-ttu-id="2ea30-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ea30-107">EXAMPLES</span></span>

### <span data-ttu-id="2ea30-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2ea30-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="2ea30-109">Obtém provedores de serviços de paração disponíveis</span><span class="sxs-lookup"><span data-stu-id="2ea30-109">Gets available peering service providers</span></span>

## <span data-ttu-id="2ea30-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2ea30-110">PARAMETERS</span></span>

### <span data-ttu-id="2ea30-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea30-111">-DefaultProfile</span></span>
<span data-ttu-id="2ea30-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ea30-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ea30-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea30-113">CommonParameters</span></span>
<span data-ttu-id="2ea30-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ea30-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea30-115">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ea30-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea30-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ea30-116">INPUTS</span></span>

### <span data-ttu-id="2ea30-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2ea30-117">None</span></span>

## <span data-ttu-id="2ea30-118">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2ea30-118">OUTPUTS</span></span>

### <span data-ttu-id="2ea30-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="2ea30-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="2ea30-120">NOTES</span><span class="sxs-lookup"><span data-stu-id="2ea30-120">NOTES</span></span>

## <span data-ttu-id="2ea30-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ea30-121">RELATED LINKS</span></span>
