---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
ms.openlocfilehash: 7c385f230456da60df76c56fc652dda53362c778
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786370"
---
# <span data-ttu-id="e26b7-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="e26b7-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="e26b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e26b7-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e26b7-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e26b7-103">SYNTAX</span></span>

### <span data-ttu-id="e26b7-104">Eles</span><span class="sxs-lookup"><span data-stu-id="e26b7-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e26b7-105">S2</span><span class="sxs-lookup"><span data-stu-id="e26b7-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e26b7-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e26b7-106">DESCRIPTION</span></span>
<span data-ttu-id="e26b7-107">O cmdlet **Reset-AzureRmWebAppSlotPublishingProfile** redefine o perfil de publicação para o slot do aplicativo Web especificado.</span><span class="sxs-lookup"><span data-stu-id="e26b7-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="e26b7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e26b7-108">EXAMPLES</span></span>

### <span data-ttu-id="e26b7-109">1:</span><span class="sxs-lookup"><span data-stu-id="e26b7-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="e26b7-110">Esse comando redefine o perfil de publicação do slot chamado slot001 para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="e26b7-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e26b7-111">OS</span><span class="sxs-lookup"><span data-stu-id="e26b7-111">PARAMETERS</span></span>

### <span data-ttu-id="e26b7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e26b7-112">-DefaultProfile</span></span>
<span data-ttu-id="e26b7-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e26b7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e26b7-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e26b7-114">-Name</span></span>
<span data-ttu-id="e26b7-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="e26b7-115">WebApp Name</span></span>

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

### <span data-ttu-id="e26b7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e26b7-116">-ResourceGroupName</span></span>
<span data-ttu-id="e26b7-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e26b7-117">Resource Group Name</span></span>

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

### <span data-ttu-id="e26b7-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="e26b7-118">-Slot</span></span>
<span data-ttu-id="e26b7-119">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="e26b7-119">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26b7-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e26b7-120">-WebApp</span></span>
<span data-ttu-id="e26b7-121">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="e26b7-121">WebApp Object</span></span>

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

### <span data-ttu-id="e26b7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e26b7-122">CommonParameters</span></span>
<span data-ttu-id="e26b7-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e26b7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e26b7-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e26b7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e26b7-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e26b7-125">INPUTS</span></span>

### <span data-ttu-id="e26b7-126">Instalação</span><span class="sxs-lookup"><span data-stu-id="e26b7-126">Site</span></span>
<span data-ttu-id="e26b7-127">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="e26b7-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e26b7-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e26b7-128">OUTPUTS</span></span>

## <span data-ttu-id="e26b7-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e26b7-129">NOTES</span></span>

## <span data-ttu-id="e26b7-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e26b7-130">RELATED LINKS</span></span>

