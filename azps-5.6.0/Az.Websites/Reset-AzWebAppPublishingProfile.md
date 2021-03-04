---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 9d3a17280f80ef0376912f806439698f24cdfe25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892677"
---
# <span data-ttu-id="042c4-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="042c4-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="042c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="042c4-102">SYNOPSIS</span></span>

## <span data-ttu-id="042c4-103">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="042c4-103">SYNTAX</span></span>

### <span data-ttu-id="042c4-104">S1</span><span class="sxs-lookup"><span data-stu-id="042c4-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="042c4-105">S2</span><span class="sxs-lookup"><span data-stu-id="042c4-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="042c4-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="042c4-106">DESCRIPTION</span></span>
<span data-ttu-id="042c4-107">O cmdlet **Reset-AzWebAppPublishingProfile** redefine o perfil de publicação do Aplicativo Web especificado.</span><span class="sxs-lookup"><span data-stu-id="042c4-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="042c4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="042c4-108">EXAMPLES</span></span>

### <span data-ttu-id="042c4-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="042c4-109">Example 1</span></span>

<span data-ttu-id="042c4-110">O exemplo a seguir redefine o perfil de publicação do IpRule do Aplicativo Web associado ao grupo de recursos MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="042c4-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="042c4-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="042c4-111">PARAMETERS</span></span>

### <span data-ttu-id="042c4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="042c4-112">-DefaultProfile</span></span>
<span data-ttu-id="042c4-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="042c4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="042c4-114">-Name</span><span class="sxs-lookup"><span data-stu-id="042c4-114">-Name</span></span>
<span data-ttu-id="042c4-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="042c4-115">WebApp Name</span></span>

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

### <span data-ttu-id="042c4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="042c4-116">-ResourceGroupName</span></span>
<span data-ttu-id="042c4-117">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="042c4-117">Resource Group Name</span></span>

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

### <span data-ttu-id="042c4-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="042c4-118">-WebApp</span></span>
<span data-ttu-id="042c4-119">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="042c4-119">WebApp Object</span></span>

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

### <span data-ttu-id="042c4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="042c4-120">CommonParameters</span></span>
<span data-ttu-id="042c4-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="042c4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="042c4-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="042c4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="042c4-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="042c4-123">INPUTS</span></span>

### <span data-ttu-id="042c4-124">System.String</span><span class="sxs-lookup"><span data-stu-id="042c4-124">System.String</span></span>

### <span data-ttu-id="042c4-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="042c4-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="042c4-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="042c4-126">OUTPUTS</span></span>

### <span data-ttu-id="042c4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="042c4-127">System.String</span></span>

## <span data-ttu-id="042c4-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="042c4-128">NOTES</span></span>

## <span data-ttu-id="042c4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="042c4-129">RELATED LINKS</span></span>
