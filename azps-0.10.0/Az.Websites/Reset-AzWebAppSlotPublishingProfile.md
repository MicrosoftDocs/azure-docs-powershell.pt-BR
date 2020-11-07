---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/reset-Azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: ec0b95ffee67d5597a06ed0729cded33e7489465
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776078"
---
# <span data-ttu-id="a84a8-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="a84a8-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="a84a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a84a8-102">SYNOPSIS</span></span>

## <span data-ttu-id="a84a8-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a84a8-103">SYNTAX</span></span>

### <span data-ttu-id="a84a8-104">Eles</span><span class="sxs-lookup"><span data-stu-id="a84a8-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a84a8-105">S2</span><span class="sxs-lookup"><span data-stu-id="a84a8-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a84a8-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a84a8-106">DESCRIPTION</span></span>
<span data-ttu-id="a84a8-107">O cmdlet **Reset-AzWebAppSlotPublishingProfile** redefine o perfil de publicação para o slot do aplicativo Web especificado.</span><span class="sxs-lookup"><span data-stu-id="a84a8-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="a84a8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a84a8-108">EXAMPLES</span></span>

### <span data-ttu-id="a84a8-109">1:</span><span class="sxs-lookup"><span data-stu-id="a84a8-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="a84a8-110">Esse comando redefine o perfil de publicação do slot chamado slot001 para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="a84a8-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a84a8-111">OS</span><span class="sxs-lookup"><span data-stu-id="a84a8-111">PARAMETERS</span></span>

### <span data-ttu-id="a84a8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a84a8-112">-DefaultProfile</span></span>
<span data-ttu-id="a84a8-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a84a8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a84a8-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="a84a8-114">-Name</span></span>
<span data-ttu-id="a84a8-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="a84a8-115">WebApp Name</span></span>

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

### <span data-ttu-id="a84a8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a84a8-116">-ResourceGroupName</span></span>
<span data-ttu-id="a84a8-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a84a8-117">Resource Group Name</span></span>

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

### <span data-ttu-id="a84a8-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="a84a8-118">-Slot</span></span>
<span data-ttu-id="a84a8-119">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="a84a8-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a84a8-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a84a8-120">-WebApp</span></span>
<span data-ttu-id="a84a8-121">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="a84a8-121">WebApp Object</span></span>

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

### <span data-ttu-id="a84a8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a84a8-122">CommonParameters</span></span>
<span data-ttu-id="a84a8-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a84a8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a84a8-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a84a8-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a84a8-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a84a8-125">INPUTS</span></span>

### <span data-ttu-id="a84a8-126">Instalação</span><span class="sxs-lookup"><span data-stu-id="a84a8-126">Site</span></span>
<span data-ttu-id="a84a8-127">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="a84a8-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a84a8-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a84a8-128">OUTPUTS</span></span>

## <span data-ttu-id="a84a8-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a84a8-129">NOTES</span></span>

## <span data-ttu-id="a84a8-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a84a8-130">RELATED LINKS</span></span>

