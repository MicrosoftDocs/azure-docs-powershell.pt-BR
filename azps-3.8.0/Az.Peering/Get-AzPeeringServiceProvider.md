---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 8341f465bab88f8d8a60e5f171f883dbb9a2467e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944476"
---
# <span data-ttu-id="60bab-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="60bab-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="60bab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60bab-102">SYNOPSIS</span></span>
<span data-ttu-id="60bab-103">Obtém uma lista de provedores de serviços de emparelhamento em parceria com a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="60bab-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="60bab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60bab-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60bab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60bab-105">DESCRIPTION</span></span>
<span data-ttu-id="60bab-106">Provedores de serviços de emparelhamento de lista</span><span class="sxs-lookup"><span data-stu-id="60bab-106">List peering service providers</span></span>

## <span data-ttu-id="60bab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60bab-107">EXAMPLES</span></span>

### <span data-ttu-id="60bab-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="60bab-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="60bab-109">Obtém provedores de serviço de emparelhamento disponíveis</span><span class="sxs-lookup"><span data-stu-id="60bab-109">Gets available peering service providers</span></span>

## <span data-ttu-id="60bab-110">OS</span><span class="sxs-lookup"><span data-stu-id="60bab-110">PARAMETERS</span></span>

### <span data-ttu-id="60bab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60bab-111">-DefaultProfile</span></span>
<span data-ttu-id="60bab-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60bab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60bab-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60bab-113">CommonParameters</span></span>
<span data-ttu-id="60bab-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60bab-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60bab-115">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60bab-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60bab-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60bab-116">INPUTS</span></span>

### <span data-ttu-id="60bab-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="60bab-117">None</span></span>

## <span data-ttu-id="60bab-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60bab-118">OUTPUTS</span></span>

### <span data-ttu-id="60bab-119">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="60bab-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="60bab-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60bab-120">NOTES</span></span>

## <span data-ttu-id="60bab-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60bab-121">RELATED LINKS</span></span>
