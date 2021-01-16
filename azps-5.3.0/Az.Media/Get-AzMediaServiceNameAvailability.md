---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271970"
---
# <span data-ttu-id="62488-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="62488-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="62488-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62488-102">SYNOPSIS</span></span>
<span data-ttu-id="62488-103">Verifica se um nome de serviço de mídia está disponível.</span><span class="sxs-lookup"><span data-stu-id="62488-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="62488-104">Os nomes de serviços de mídia são exclusivos globalmente.</span><span class="sxs-lookup"><span data-stu-id="62488-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="62488-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62488-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="62488-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62488-106">DESCRIPTION</span></span>
<span data-ttu-id="62488-107">O cmdlet **Get-AzMediaServiceNameAvailability** verifica se um nome de serviço de mídia está disponível.</span><span class="sxs-lookup"><span data-stu-id="62488-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="62488-108">Os nomes de serviços de mídia são exclusivos globalmente.</span><span class="sxs-lookup"><span data-stu-id="62488-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="62488-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62488-109">EXAMPLES</span></span>

### <span data-ttu-id="62488-110">Exemplo 1: verificar se um nome de serviço de mídia está disponível</span><span class="sxs-lookup"><span data-stu-id="62488-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="62488-111">Esse comando verifica se o nome MediaService1 está disponível.</span><span class="sxs-lookup"><span data-stu-id="62488-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="62488-112">OS</span><span class="sxs-lookup"><span data-stu-id="62488-112">PARAMETERS</span></span>

### <span data-ttu-id="62488-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="62488-113">-AccountName</span></span>
<span data-ttu-id="62488-114">Especifica o nome do serviço de mídia que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="62488-114">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62488-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62488-115">-DefaultProfile</span></span>
<span data-ttu-id="62488-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="62488-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62488-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62488-117">CommonParameters</span></span>
<span data-ttu-id="62488-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62488-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62488-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62488-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62488-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62488-120">INPUTS</span></span>

### <span data-ttu-id="62488-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="62488-121">None</span></span>

## <span data-ttu-id="62488-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62488-122">OUTPUTS</span></span>

### <span data-ttu-id="62488-123">Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="62488-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="62488-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62488-124">NOTES</span></span>

## <span data-ttu-id="62488-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62488-125">RELATED LINKS</span></span>

[<span data-ttu-id="62488-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="62488-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="62488-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="62488-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="62488-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="62488-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="62488-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="62488-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


