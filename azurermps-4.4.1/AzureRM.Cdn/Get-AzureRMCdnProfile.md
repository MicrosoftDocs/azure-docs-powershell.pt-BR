---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: 726e84e1fe43e90ebf16241a017dadb2af5584b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440207"
---
# <span data-ttu-id="70a08-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="70a08-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="70a08-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70a08-102">SYNOPSIS</span></span>
<span data-ttu-id="70a08-103">Obtém um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="70a08-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70a08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70a08-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70a08-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70a08-105">DESCRIPTION</span></span>
<span data-ttu-id="70a08-106">O cmdlet **Get-AzureRMCdnProfile** Obtém um perfil da CDN (rede de distribuição de conteúdo) do Azure e suas informações relacionadas.</span><span class="sxs-lookup"><span data-stu-id="70a08-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="70a08-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70a08-107">EXAMPLES</span></span>

## <span data-ttu-id="70a08-108">OS</span><span class="sxs-lookup"><span data-stu-id="70a08-108">PARAMETERS</span></span>

### <span data-ttu-id="70a08-109">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="70a08-109">-ProfileName</span></span>
<span data-ttu-id="70a08-110">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="70a08-110">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a08-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70a08-111">-ResourceGroupName</span></span>
<span data-ttu-id="70a08-112">Especifica o nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="70a08-112">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a08-113">-DefaultProfile</span></span>
<span data-ttu-id="70a08-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70a08-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70a08-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a08-115">CommonParameters</span></span>
<span data-ttu-id="70a08-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70a08-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70a08-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70a08-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a08-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70a08-118">INPUTS</span></span>

## <span data-ttu-id="70a08-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70a08-119">OUTPUTS</span></span>

###  
<span data-ttu-id="70a08-120">Esse cmdlet retorna um objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="70a08-120">This cmdlet returns a profile object.</span></span>

## <span data-ttu-id="70a08-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70a08-121">NOTES</span></span>

## <span data-ttu-id="70a08-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70a08-122">RELATED LINKS</span></span>

[<span data-ttu-id="70a08-123">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="70a08-123">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="70a08-124">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="70a08-124">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="70a08-125">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="70a08-125">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


