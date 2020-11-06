---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: c554caf7230b54db3e1161a20e001f9873f6dfff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431131"
---
# <span data-ttu-id="af649-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="af649-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="af649-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af649-102">SYNOPSIS</span></span>
<span data-ttu-id="af649-103">Atualiza um servidor de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="af649-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af649-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af649-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af649-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af649-105">DESCRIPTION</span></span>
<span data-ttu-id="af649-106">O cmdlet **set-AzureRmCdnOrigin** atualiza um servidor de origem da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="af649-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="af649-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af649-107">EXAMPLES</span></span>

## <span data-ttu-id="af649-108">OS</span><span class="sxs-lookup"><span data-stu-id="af649-108">PARAMETERS</span></span>

### <span data-ttu-id="af649-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="af649-109">-CdnOrigin</span></span>
<span data-ttu-id="af649-110">Especifica o servidor de origem no qual esse cmdlet é atualizado.</span><span class="sxs-lookup"><span data-stu-id="af649-110">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="af649-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af649-111">-DefaultProfile</span></span>
<span data-ttu-id="af649-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af649-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af649-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af649-113">CommonParameters</span></span>
<span data-ttu-id="af649-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af649-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af649-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af649-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af649-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af649-116">INPUTS</span></span>

### <span data-ttu-id="af649-117">PSOrigin</span><span class="sxs-lookup"><span data-stu-id="af649-117">PSOrigin</span></span>
<span data-ttu-id="af649-118">O parâmetro ' CdnOrigin' aceita o valor do tipo ' PSOrigin' do pipeline</span><span class="sxs-lookup"><span data-stu-id="af649-118">Parameter 'CdnOrigin' accepts value of type 'PSOrigin' from the pipeline</span></span>

## <span data-ttu-id="af649-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af649-119">OUTPUTS</span></span>

### <span data-ttu-id="af649-120">Microsoft. Azure. Commands. cdn. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="af649-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="af649-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af649-121">NOTES</span></span>

## <span data-ttu-id="af649-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af649-122">RELATED LINKS</span></span>

[<span data-ttu-id="af649-123">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="af649-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)


