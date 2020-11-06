---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: 096b062325ddfa12eba1d8c0fe8d6a154c3e77fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430784"
---
# <span data-ttu-id="1467d-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="1467d-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="1467d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1467d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1467d-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1467d-103">SYNTAX</span></span>

### <span data-ttu-id="1467d-104">Eles</span><span class="sxs-lookup"><span data-stu-id="1467d-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1467d-105">S2</span><span class="sxs-lookup"><span data-stu-id="1467d-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1467d-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1467d-106">DESCRIPTION</span></span>
<span data-ttu-id="1467d-107">O cmdlet **Reset-AzureRmWebAppPublishingProfile** redefine o perfil de publicação do aplicativo Web especificado.</span><span class="sxs-lookup"><span data-stu-id="1467d-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="1467d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1467d-108">EXAMPLES</span></span>

### <span data-ttu-id="1467d-109">1:</span><span class="sxs-lookup"><span data-stu-id="1467d-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="1467d-110">Esse comando redefine o perfil de publicação do aplicativo Web ContosoWebApp associado ao grupo de recursos padrão-oeste-Web-oeste.</span><span class="sxs-lookup"><span data-stu-id="1467d-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1467d-111">OS</span><span class="sxs-lookup"><span data-stu-id="1467d-111">PARAMETERS</span></span>

### <span data-ttu-id="1467d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1467d-112">-DefaultProfile</span></span>
<span data-ttu-id="1467d-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1467d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1467d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="1467d-114">-Name</span></span>
<span data-ttu-id="1467d-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="1467d-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1467d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1467d-116">-ResourceGroupName</span></span>
<span data-ttu-id="1467d-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1467d-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1467d-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1467d-118">-WebApp</span></span>
<span data-ttu-id="1467d-119">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="1467d-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1467d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1467d-120">CommonParameters</span></span>
<span data-ttu-id="1467d-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1467d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1467d-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1467d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1467d-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1467d-123">INPUTS</span></span>

### <span data-ttu-id="1467d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1467d-124">System.String</span></span>

### <span data-ttu-id="1467d-125">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="1467d-125">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="1467d-126">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1467d-126">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="1467d-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1467d-127">OUTPUTS</span></span>

### <span data-ttu-id="1467d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1467d-128">System.String</span></span>

## <span data-ttu-id="1467d-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1467d-129">NOTES</span></span>

## <span data-ttu-id="1467d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1467d-130">RELATED LINKS</span></span>
