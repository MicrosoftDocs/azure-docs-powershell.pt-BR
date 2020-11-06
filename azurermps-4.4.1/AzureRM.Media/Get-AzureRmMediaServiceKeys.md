---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 6cef357b636a48e433d545a56d2b5105556842da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610757"
---
# <span data-ttu-id="1a052-101">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="1a052-101">Get-AzureRmMediaServiceKeys</span></span>

## <span data-ttu-id="1a052-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a052-102">SYNOPSIS</span></span>
<span data-ttu-id="1a052-103">Obtém informações importantes para acessar o ponto de extremidade REST associado ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="1a052-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a052-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a052-104">SYNTAX</span></span>

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a052-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a052-105">DESCRIPTION</span></span>
<span data-ttu-id="1a052-106">O cmdlet **Get-AzureRmMediaServiceKeys** Obtém informações importantes para acessar o ponto de extremidade do REST (transferência de estado representational) associado ao serviço de mídia do Azure.</span><span class="sxs-lookup"><span data-stu-id="1a052-106">The **Get-AzureRmMediaServiceKeys** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="1a052-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a052-107">EXAMPLES</span></span>

### <span data-ttu-id="1a052-108">Exemplo 1: obter as informações importantes para acessar o serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="1a052-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="1a052-109">Esse comando obtém as informações importantes para acessar o serviço de mídia chamado MediaService001 que pertence ao grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="1a052-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="1a052-110">OS</span><span class="sxs-lookup"><span data-stu-id="1a052-110">PARAMETERS</span></span>

### <span data-ttu-id="1a052-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1a052-111">-AccountName</span></span>
<span data-ttu-id="1a052-112">Especifica o nome do serviço de mídia do qual este cmdlet obtém as chaves de serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="1a052-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a052-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a052-113">-ResourceGroupName</span></span>
<span data-ttu-id="1a052-114">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="1a052-114">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a052-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a052-115">-DefaultProfile</span></span>
<span data-ttu-id="1a052-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a052-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a052-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a052-117">CommonParameters</span></span>
<span data-ttu-id="1a052-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a052-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a052-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a052-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a052-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a052-120">INPUTS</span></span>

## <span data-ttu-id="1a052-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a052-121">OUTPUTS</span></span>

### <span data-ttu-id="1a052-122">Microsoft. Azure. Commands. Media. Models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="1a052-122">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="1a052-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a052-123">NOTES</span></span>

## <span data-ttu-id="1a052-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a052-124">RELATED LINKS</span></span>

[<span data-ttu-id="1a052-125">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="1a052-125">Set-AzureRmMediaServiceKey</span></span>](./Set-AzureRmMediaServiceKey.md)


