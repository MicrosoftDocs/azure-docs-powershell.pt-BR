---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
ms.openlocfilehash: f082241be9e31b11782fcbbf5570a7f3c3947012
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785130"
---
# <span data-ttu-id="07528-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="07528-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="07528-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07528-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07528-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07528-103">SYNTAX</span></span>

### <span data-ttu-id="07528-104">Eles</span><span class="sxs-lookup"><span data-stu-id="07528-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07528-105">S2</span><span class="sxs-lookup"><span data-stu-id="07528-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07528-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07528-106">DESCRIPTION</span></span>
<span data-ttu-id="07528-107">O cmdlet **Reset-AzureRmWebAppPublishingProfile** redefine o perfil de publicação do aplicativo Web especificado.</span><span class="sxs-lookup"><span data-stu-id="07528-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="07528-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07528-108">EXAMPLES</span></span>

### <span data-ttu-id="07528-109">1:</span><span class="sxs-lookup"><span data-stu-id="07528-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="07528-110">Esse comando redefine o perfil de publicação do aplicativo Web ContosoWebApp associado ao grupo de recursos padrão-oeste-Web-oeste.</span><span class="sxs-lookup"><span data-stu-id="07528-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="07528-111">OS</span><span class="sxs-lookup"><span data-stu-id="07528-111">PARAMETERS</span></span>

### <span data-ttu-id="07528-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07528-112">-DefaultProfile</span></span>
<span data-ttu-id="07528-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07528-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07528-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="07528-114">-Name</span></span>
<span data-ttu-id="07528-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="07528-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07528-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07528-116">-ResourceGroupName</span></span>
<span data-ttu-id="07528-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="07528-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07528-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="07528-118">-WebApp</span></span>
<span data-ttu-id="07528-119">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="07528-119">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07528-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07528-120">CommonParameters</span></span>
<span data-ttu-id="07528-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07528-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07528-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07528-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07528-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07528-123">INPUTS</span></span>

### <span data-ttu-id="07528-124">Instalação</span><span class="sxs-lookup"><span data-stu-id="07528-124">Site</span></span>
<span data-ttu-id="07528-125">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="07528-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="07528-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07528-126">OUTPUTS</span></span>

## <span data-ttu-id="07528-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07528-127">NOTES</span></span>

## <span data-ttu-id="07528-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07528-128">RELATED LINKS</span></span>

