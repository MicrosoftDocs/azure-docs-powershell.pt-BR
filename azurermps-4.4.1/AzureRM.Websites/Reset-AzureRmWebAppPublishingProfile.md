---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: f1224ae7ad95598d8ae947d0e38ef3a9cf7a4dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428233"
---
# <span data-ttu-id="ef161-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="ef161-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="ef161-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef161-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef161-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef161-103">SYNTAX</span></span>

### <span data-ttu-id="ef161-104">Eles</span><span class="sxs-lookup"><span data-stu-id="ef161-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef161-105">S2</span><span class="sxs-lookup"><span data-stu-id="ef161-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef161-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef161-106">DESCRIPTION</span></span>
<span data-ttu-id="ef161-107">O cmdlet **Reset-AzureRmWebAppPublishingProfile** redefine o perfil de publicação do aplicativo Web especificado.</span><span class="sxs-lookup"><span data-stu-id="ef161-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="ef161-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef161-108">EXAMPLES</span></span>

### <span data-ttu-id="ef161-109">1:</span><span class="sxs-lookup"><span data-stu-id="ef161-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="ef161-110">Esse comando redefine o perfil de publicação do aplicativo Web ContosoWebApp associado ao grupo de recursos padrão-oeste-Web-oeste.</span><span class="sxs-lookup"><span data-stu-id="ef161-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="ef161-111">OS</span><span class="sxs-lookup"><span data-stu-id="ef161-111">PARAMETERS</span></span>

### <span data-ttu-id="ef161-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef161-112">-Name</span></span>
<span data-ttu-id="ef161-113">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="ef161-113">WebApp Name</span></span>

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

### <span data-ttu-id="ef161-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef161-114">-ResourceGroupName</span></span>
<span data-ttu-id="ef161-115">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ef161-115">Resource Group Name</span></span>

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

### <span data-ttu-id="ef161-116">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ef161-116">-WebApp</span></span>
<span data-ttu-id="ef161-117">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="ef161-117">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef161-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef161-118">-DefaultProfile</span></span>
<span data-ttu-id="ef161-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef161-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef161-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef161-120">CommonParameters</span></span>
<span data-ttu-id="ef161-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef161-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef161-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef161-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef161-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef161-123">INPUTS</span></span>

### <span data-ttu-id="ef161-124">Instalação</span><span class="sxs-lookup"><span data-stu-id="ef161-124">Site</span></span>
<span data-ttu-id="ef161-125">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="ef161-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ef161-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef161-126">OUTPUTS</span></span>

## <span data-ttu-id="ef161-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef161-127">NOTES</span></span>

## <span data-ttu-id="ef161-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef161-128">RELATED LINKS</span></span>

