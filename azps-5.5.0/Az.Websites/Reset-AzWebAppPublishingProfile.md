---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81005ceac6bfa3c258a147f3fbef168e95c302cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118839"
---
# <span data-ttu-id="bb912-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="bb912-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="bb912-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb912-102">SYNOPSIS</span></span>

## <span data-ttu-id="bb912-103">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb912-103">SYNTAX</span></span>

### <span data-ttu-id="bb912-104">S1</span><span class="sxs-lookup"><span data-stu-id="bb912-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb912-105">S2</span><span class="sxs-lookup"><span data-stu-id="bb912-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb912-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb912-106">DESCRIPTION</span></span>
<span data-ttu-id="bb912-107">O cmdlet **Reset-AzWebAppPublishingProfile** redefine o perfil de publicação do Web App especificado.</span><span class="sxs-lookup"><span data-stu-id="bb912-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="bb912-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bb912-108">EXAMPLES</span></span>

### <span data-ttu-id="bb912-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb912-109">Example 1</span></span>

<span data-ttu-id="bb912-110">O exemplo a seguir redefine o perfil de publicação do IpRule do Web App associado ao grupo de recursos MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bb912-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="bb912-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb912-111">PARAMETERS</span></span>

### <span data-ttu-id="bb912-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb912-112">-DefaultProfile</span></span>
<span data-ttu-id="bb912-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bb912-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb912-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb912-114">-Name</span></span>
<span data-ttu-id="bb912-115">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="bb912-115">WebApp Name</span></span>

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

### <span data-ttu-id="bb912-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb912-116">-ResourceGroupName</span></span>
<span data-ttu-id="bb912-117">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="bb912-117">Resource Group Name</span></span>

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

### <span data-ttu-id="bb912-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bb912-118">-WebApp</span></span>
<span data-ttu-id="bb912-119">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="bb912-119">WebApp Object</span></span>

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

### <span data-ttu-id="bb912-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb912-120">CommonParameters</span></span>
<span data-ttu-id="bb912-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb912-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb912-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb912-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb912-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="bb912-123">INPUTS</span></span>

### <span data-ttu-id="bb912-124">System.String</span><span class="sxs-lookup"><span data-stu-id="bb912-124">System.String</span></span>

### <span data-ttu-id="bb912-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="bb912-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="bb912-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="bb912-126">OUTPUTS</span></span>

### <span data-ttu-id="bb912-127">System.String</span><span class="sxs-lookup"><span data-stu-id="bb912-127">System.String</span></span>

## <span data-ttu-id="bb912-128">Notas</span><span class="sxs-lookup"><span data-stu-id="bb912-128">NOTES</span></span>

## <span data-ttu-id="bb912-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb912-129">RELATED LINKS</span></span>
