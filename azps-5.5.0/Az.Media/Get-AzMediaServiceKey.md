---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: a01aeaa5868ece4f376dd5be934ba1029379958b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111780"
---
# <span data-ttu-id="29ee1-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="29ee1-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="29ee1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="29ee1-103">Obtém informações importantes para acessar o ponto de extremidade REST associado ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="29ee1-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="29ee1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29ee1-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29ee1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="29ee1-105">DESCRIPTION</span></span>
<span data-ttu-id="29ee1-106">O cmdlet **Get-AzMediaServiceKey** obtém informações importantes para acessar o ponto de extremidade REST (Representational State Transfer) associado ao serviço de mídia do Azure.</span><span class="sxs-lookup"><span data-stu-id="29ee1-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="29ee1-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="29ee1-107">EXAMPLES</span></span>

### <span data-ttu-id="29ee1-108">Exemplo 1: Obter as principais informações para acessar o serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="29ee1-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="29ee1-109">Esse comando obtém as principais informações para acessar o serviço de mídia chamado MediaService001 que pertence ao grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="29ee1-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="29ee1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29ee1-110">PARAMETERS</span></span>

### <span data-ttu-id="29ee1-111">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="29ee1-111">-AccountName</span></span>
<span data-ttu-id="29ee1-112">Especifica o nome do serviço de mídia de onde este cmdlet obtém as chaves de serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="29ee1-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="29ee1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ee1-113">-DefaultProfile</span></span>
<span data-ttu-id="29ee1-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="29ee1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29ee1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29ee1-115">-ResourceGroupName</span></span>
<span data-ttu-id="29ee1-116">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="29ee1-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="29ee1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ee1-117">CommonParameters</span></span>
<span data-ttu-id="29ee1-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29ee1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ee1-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29ee1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ee1-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="29ee1-120">INPUTS</span></span>

### <span data-ttu-id="29ee1-121">System.String</span><span class="sxs-lookup"><span data-stu-id="29ee1-121">System.String</span></span>

## <span data-ttu-id="29ee1-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="29ee1-122">OUTPUTS</span></span>

### <span data-ttu-id="29ee1-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="29ee1-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="29ee1-124">Notas</span><span class="sxs-lookup"><span data-stu-id="29ee1-124">NOTES</span></span>

## <span data-ttu-id="29ee1-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29ee1-125">RELATED LINKS</span></span>

[<span data-ttu-id="29ee1-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="29ee1-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


