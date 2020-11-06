---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 948088f99e90af4594e239dc379133955340e1d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430782"
---
# <span data-ttu-id="3c4da-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="3c4da-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="3c4da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c4da-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c4da-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c4da-103">SYNTAX</span></span>

### <span data-ttu-id="3c4da-104">Eles</span><span class="sxs-lookup"><span data-stu-id="3c4da-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c4da-105">S2</span><span class="sxs-lookup"><span data-stu-id="3c4da-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c4da-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c4da-106">DESCRIPTION</span></span>
<span data-ttu-id="3c4da-107">O cmdlet **Reset-AzureRmWebAppSlotPublishingProfile** redefine o perfil de publicação para o slot do aplicativo Web especificado.</span><span class="sxs-lookup"><span data-stu-id="3c4da-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="3c4da-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c4da-108">EXAMPLES</span></span>

### <span data-ttu-id="3c4da-109">1:</span><span class="sxs-lookup"><span data-stu-id="3c4da-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="3c4da-110">Esse comando redefine o perfil de publicação do slot chamado slot001 para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="3c4da-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="3c4da-111">OS</span><span class="sxs-lookup"><span data-stu-id="3c4da-111">PARAMETERS</span></span>

### <span data-ttu-id="3c4da-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c4da-112">-DefaultProfile</span></span>
<span data-ttu-id="3c4da-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c4da-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c4da-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c4da-114">-Name</span></span>
<span data-ttu-id="3c4da-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="3c4da-115">WebApp Name</span></span>

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

### <span data-ttu-id="3c4da-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c4da-116">-ResourceGroupName</span></span>
<span data-ttu-id="3c4da-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3c4da-117">Resource Group Name</span></span>

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

### <span data-ttu-id="3c4da-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="3c4da-118">-Slot</span></span>
<span data-ttu-id="3c4da-119">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="3c4da-119">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c4da-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3c4da-120">-WebApp</span></span>
<span data-ttu-id="3c4da-121">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="3c4da-121">WebApp Object</span></span>

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

### <span data-ttu-id="3c4da-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c4da-122">CommonParameters</span></span>
<span data-ttu-id="3c4da-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c4da-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c4da-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c4da-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c4da-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c4da-125">INPUTS</span></span>

### <span data-ttu-id="3c4da-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3c4da-126">System.String</span></span>

### <span data-ttu-id="3c4da-127">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="3c4da-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="3c4da-128">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3c4da-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="3c4da-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c4da-129">OUTPUTS</span></span>

### <span data-ttu-id="3c4da-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3c4da-130">System.String</span></span>

## <span data-ttu-id="3c4da-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c4da-131">NOTES</span></span>

## <span data-ttu-id="3c4da-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c4da-132">RELATED LINKS</span></span>
