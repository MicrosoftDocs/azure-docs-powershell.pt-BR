---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: bdee1c1fdda561d7265b3f6ff52a443238b6d2b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891067"
---
# <span data-ttu-id="5318d-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="5318d-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="5318d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5318d-102">SYNOPSIS</span></span>

## <span data-ttu-id="5318d-103">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5318d-103">SYNTAX</span></span>

### <span data-ttu-id="5318d-104">S1</span><span class="sxs-lookup"><span data-stu-id="5318d-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5318d-105">S2</span><span class="sxs-lookup"><span data-stu-id="5318d-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5318d-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5318d-106">DESCRIPTION</span></span>
<span data-ttu-id="5318d-107">O cmdlet **Reset-AzWebAppSlotPublishingProfile** redefine o perfil de publicação do Slot de Aplicativo Web especificado.</span><span class="sxs-lookup"><span data-stu-id="5318d-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="5318d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5318d-108">EXAMPLES</span></span>

### <span data-ttu-id="5318d-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5318d-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="5318d-110">Este comando redefine o perfil de publicação do Slot chamado slot001 para o Web App ContosoWebApp associado ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="5318d-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5318d-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5318d-111">PARAMETERS</span></span>

### <span data-ttu-id="5318d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5318d-112">-DefaultProfile</span></span>
<span data-ttu-id="5318d-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5318d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5318d-114">-Name</span><span class="sxs-lookup"><span data-stu-id="5318d-114">-Name</span></span>
<span data-ttu-id="5318d-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="5318d-115">WebApp Name</span></span>

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

### <span data-ttu-id="5318d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5318d-116">-ResourceGroupName</span></span>
<span data-ttu-id="5318d-117">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="5318d-117">Resource Group Name</span></span>

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

### <span data-ttu-id="5318d-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="5318d-118">-Slot</span></span>
<span data-ttu-id="5318d-119">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="5318d-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="5318d-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5318d-120">-WebApp</span></span>
<span data-ttu-id="5318d-121">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="5318d-121">WebApp Object</span></span>

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

### <span data-ttu-id="5318d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5318d-122">CommonParameters</span></span>
<span data-ttu-id="5318d-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5318d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5318d-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5318d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5318d-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5318d-125">INPUTS</span></span>

### <span data-ttu-id="5318d-126">System.String</span><span class="sxs-lookup"><span data-stu-id="5318d-126">System.String</span></span>

### <span data-ttu-id="5318d-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="5318d-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5318d-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5318d-128">OUTPUTS</span></span>

### <span data-ttu-id="5318d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5318d-129">System.String</span></span>

## <span data-ttu-id="5318d-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="5318d-130">NOTES</span></span>

## <span data-ttu-id="5318d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5318d-131">RELATED LINKS</span></span>
