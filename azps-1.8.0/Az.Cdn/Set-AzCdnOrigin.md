---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 74af4f7c4bc4f211f22be111bff4ecf0a8b9831a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771268"
---
# <span data-ttu-id="9b802-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="9b802-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="9b802-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b802-102">SYNOPSIS</span></span>
<span data-ttu-id="9b802-103">Atualiza um servidor de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="9b802-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="9b802-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b802-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b802-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b802-105">DESCRIPTION</span></span>
<span data-ttu-id="9b802-106">O cmdlet **set-AzCdnOrigin** atualiza um servidor de origem da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="9b802-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="9b802-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b802-107">EXAMPLES</span></span>

## <span data-ttu-id="9b802-108">OS</span><span class="sxs-lookup"><span data-stu-id="9b802-108">PARAMETERS</span></span>

### <span data-ttu-id="9b802-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="9b802-109">-CdnOrigin</span></span>
<span data-ttu-id="9b802-110">Especifica o servidor de origem no qual esse cmdlet é atualizado.</span><span class="sxs-lookup"><span data-stu-id="9b802-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b802-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b802-111">-DefaultProfile</span></span>
<span data-ttu-id="9b802-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9b802-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b802-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b802-113">CommonParameters</span></span>
<span data-ttu-id="9b802-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b802-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b802-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b802-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b802-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b802-116">INPUTS</span></span>

### <span data-ttu-id="9b802-117">Microsoft. Azure. Commands. cdn. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="9b802-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="9b802-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b802-118">OUTPUTS</span></span>

### <span data-ttu-id="9b802-119">Microsoft. Azure. Commands. cdn. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="9b802-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="9b802-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b802-120">NOTES</span></span>

## <span data-ttu-id="9b802-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b802-121">RELATED LINKS</span></span>

[<span data-ttu-id="9b802-122">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="9b802-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


