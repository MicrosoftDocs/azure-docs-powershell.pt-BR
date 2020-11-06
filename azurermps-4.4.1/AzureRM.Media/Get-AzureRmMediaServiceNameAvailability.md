---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: be459183e47982fef8dbd2376ddd5110251bb001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609643"
---
# <span data-ttu-id="450f4-101">Get-AzureRmMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="450f4-101">Get-AzureRmMediaServiceNameAvailability</span></span>

## <span data-ttu-id="450f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="450f4-102">SYNOPSIS</span></span>
<span data-ttu-id="450f4-103">Verifica se um nome de serviço de mídia está disponível.</span><span class="sxs-lookup"><span data-stu-id="450f4-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="450f4-104">Os nomes de serviços de mídia são exclusivos globalmente.</span><span class="sxs-lookup"><span data-stu-id="450f4-104">Media service names are globally unique.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="450f4-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="450f4-105">SYNTAX</span></span>

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="450f4-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="450f4-106">DESCRIPTION</span></span>
<span data-ttu-id="450f4-107">O cmdlet **Get-AzureRmMediaServiceNameAvailability** verifica se um nome de serviço de mídia está disponível.</span><span class="sxs-lookup"><span data-stu-id="450f4-107">The **Get-AzureRmMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="450f4-108">Os nomes de serviços de mídia são exclusivos globalmente.</span><span class="sxs-lookup"><span data-stu-id="450f4-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="450f4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="450f4-109">EXAMPLES</span></span>

### <span data-ttu-id="450f4-110">Exemplo 1: verificar se um nome de serviço de mídia está disponível</span><span class="sxs-lookup"><span data-stu-id="450f4-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="450f4-111">Esse comando verifica se o nome MediaService1 está disponível.</span><span class="sxs-lookup"><span data-stu-id="450f4-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="450f4-112">OS</span><span class="sxs-lookup"><span data-stu-id="450f4-112">PARAMETERS</span></span>

### <span data-ttu-id="450f4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="450f4-113">-AccountName</span></span>
<span data-ttu-id="450f4-114">Especifica o nome do serviço de mídia que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="450f4-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="450f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450f4-115">-DefaultProfile</span></span>
<span data-ttu-id="450f4-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="450f4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="450f4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450f4-117">CommonParameters</span></span>
<span data-ttu-id="450f4-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="450f4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450f4-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="450f4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450f4-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="450f4-120">INPUTS</span></span>

## <span data-ttu-id="450f4-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="450f4-121">OUTPUTS</span></span>

### <span data-ttu-id="450f4-122">Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="450f4-122">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="450f4-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="450f4-123">NOTES</span></span>

## <span data-ttu-id="450f4-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="450f4-124">RELATED LINKS</span></span>

[<span data-ttu-id="450f4-125">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="450f4-125">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="450f4-126">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="450f4-126">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="450f4-127">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="450f4-127">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="450f4-128">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="450f4-128">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


