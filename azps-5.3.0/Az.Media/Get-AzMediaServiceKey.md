---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: a01aeaa5868ece4f376dd5be934ba1029379958b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428261"
---
# <span data-ttu-id="cb992-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="cb992-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="cb992-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb992-102">SYNOPSIS</span></span>
<span data-ttu-id="cb992-103">Obtém informações importantes para acessar o ponto de extremidade REST associado ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="cb992-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="cb992-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb992-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb992-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb992-105">DESCRIPTION</span></span>
<span data-ttu-id="cb992-106">O cmdlet **Get-AzMediaServiceKey** Obtém informações importantes para acessar o ponto de extremidade do REST (transferência de estado representational) associado ao serviço de mídia do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb992-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="cb992-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb992-107">EXAMPLES</span></span>

### <span data-ttu-id="cb992-108">Exemplo 1: obter as informações importantes para acessar o serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="cb992-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="cb992-109">Esse comando obtém as informações importantes para acessar o serviço de mídia chamado MediaService001 que pertence ao grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="cb992-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="cb992-110">OS</span><span class="sxs-lookup"><span data-stu-id="cb992-110">PARAMETERS</span></span>

### <span data-ttu-id="cb992-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cb992-111">-AccountName</span></span>
<span data-ttu-id="cb992-112">Especifica o nome do serviço de mídia do qual este cmdlet obtém as chaves de serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="cb992-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="cb992-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb992-113">-DefaultProfile</span></span>
<span data-ttu-id="cb992-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cb992-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb992-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb992-115">-ResourceGroupName</span></span>
<span data-ttu-id="cb992-116">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="cb992-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="cb992-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb992-117">CommonParameters</span></span>
<span data-ttu-id="cb992-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb992-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb992-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb992-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb992-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb992-120">INPUTS</span></span>

### <span data-ttu-id="cb992-121">System. String</span><span class="sxs-lookup"><span data-stu-id="cb992-121">System.String</span></span>

## <span data-ttu-id="cb992-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb992-122">OUTPUTS</span></span>

### <span data-ttu-id="cb992-123">Microsoft. Azure. Commands. Media. Models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="cb992-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="cb992-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb992-124">NOTES</span></span>

## <span data-ttu-id="cb992-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb992-125">RELATED LINKS</span></span>

[<span data-ttu-id="cb992-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="cb992-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


