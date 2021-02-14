---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 8341f465bab88f8d8a60e5f171f883dbb9a2467e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117287"
---
# <span data-ttu-id="b99b0-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b99b0-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="b99b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b99b0-102">SYNOPSIS</span></span>
<span data-ttu-id="b99b0-103">Obtém uma lista de provedores de serviços de pares em parceria com a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b99b0-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="b99b0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b99b0-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b99b0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b99b0-105">DESCRIPTION</span></span>
<span data-ttu-id="b99b0-106">Listar provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="b99b0-106">List peering service providers</span></span>

## <span data-ttu-id="b99b0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b99b0-107">EXAMPLES</span></span>

### <span data-ttu-id="b99b0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b99b0-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="b99b0-109">Obtém provedores de serviços de peering disponíveis</span><span class="sxs-lookup"><span data-stu-id="b99b0-109">Gets available peering service providers</span></span>

## <span data-ttu-id="b99b0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b99b0-110">PARAMETERS</span></span>

### <span data-ttu-id="b99b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b99b0-111">-DefaultProfile</span></span>
<span data-ttu-id="b99b0-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b99b0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b99b0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b99b0-113">CommonParameters</span></span>
<span data-ttu-id="b99b0-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b99b0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b99b0-115">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b99b0-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b99b0-116">Entradas</span><span class="sxs-lookup"><span data-stu-id="b99b0-116">INPUTS</span></span>

### <span data-ttu-id="b99b0-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b99b0-117">None</span></span>

## <span data-ttu-id="b99b0-118">Saídas</span><span class="sxs-lookup"><span data-stu-id="b99b0-118">OUTPUTS</span></span>

### <span data-ttu-id="b99b0-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b99b0-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="b99b0-120">Notas</span><span class="sxs-lookup"><span data-stu-id="b99b0-120">NOTES</span></span>

## <span data-ttu-id="b99b0-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b99b0-121">RELATED LINKS</span></span>
