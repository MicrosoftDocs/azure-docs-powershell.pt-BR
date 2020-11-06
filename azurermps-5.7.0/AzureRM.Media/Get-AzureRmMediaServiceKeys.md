---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 368423076003b03524272977ff8721db57721232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430445"
---
# <span data-ttu-id="3ca86-101">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="3ca86-101">Get-AzureRmMediaServiceKeys</span></span>

## <span data-ttu-id="3ca86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ca86-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca86-103">Obtém informações importantes para acessar o ponto de extremidade REST associado ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="3ca86-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ca86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ca86-104">SYNTAX</span></span>

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ca86-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ca86-105">DESCRIPTION</span></span>
<span data-ttu-id="3ca86-106">O cmdlet **Get-AzureRmMediaServiceKeys** Obtém informações importantes para acessar o ponto de extremidade do REST (transferência de estado representational) associado ao serviço de mídia do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca86-106">The **Get-AzureRmMediaServiceKeys** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="3ca86-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ca86-107">EXAMPLES</span></span>

### <span data-ttu-id="3ca86-108">Exemplo 1: obter as informações importantes para acessar o serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="3ca86-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="3ca86-109">Esse comando obtém as informações importantes para acessar o serviço de mídia chamado MediaService001 que pertence ao grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="3ca86-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="3ca86-110">OS</span><span class="sxs-lookup"><span data-stu-id="3ca86-110">PARAMETERS</span></span>

### <span data-ttu-id="3ca86-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3ca86-111">-AccountName</span></span>
<span data-ttu-id="3ca86-112">Especifica o nome do serviço de mídia do qual este cmdlet obtém as chaves de serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="3ca86-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca86-113">-DefaultProfile</span></span>
<span data-ttu-id="3ca86-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3ca86-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca86-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca86-115">-ResourceGroupName</span></span>
<span data-ttu-id="3ca86-116">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="3ca86-116">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca86-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca86-117">CommonParameters</span></span>
<span data-ttu-id="3ca86-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca86-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca86-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ca86-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca86-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ca86-120">INPUTS</span></span>

### <span data-ttu-id="3ca86-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3ca86-121">None</span></span>
<span data-ttu-id="3ca86-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3ca86-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ca86-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ca86-123">OUTPUTS</span></span>

### <span data-ttu-id="3ca86-124">Microsoft. Azure. Commands. Media. Models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="3ca86-124">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="3ca86-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ca86-125">NOTES</span></span>

## <span data-ttu-id="3ca86-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ca86-126">RELATED LINKS</span></span>

[<span data-ttu-id="3ca86-127">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="3ca86-127">Set-AzureRmMediaServiceKey</span></span>](./Set-AzureRmMediaServiceKey.md)


