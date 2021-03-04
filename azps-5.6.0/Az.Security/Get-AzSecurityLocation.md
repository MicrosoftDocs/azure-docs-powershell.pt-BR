---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: b835113b07fb2295193b89fd817ba82ceca71655
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891087"
---
# <span data-ttu-id="a6c27-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="a6c27-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="a6c27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6c27-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c27-103">Obtém o local onde o Centro de Segurança do Azure salvará automaticamente dados para a assinatura específica</span><span class="sxs-lookup"><span data-stu-id="a6c27-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="a6c27-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a6c27-104">SYNTAX</span></span>

### <span data-ttu-id="a6c27-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a6c27-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6c27-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a6c27-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6c27-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6c27-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6c27-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a6c27-108">DESCRIPTION</span></span>
<span data-ttu-id="a6c27-109">O Centro de Segurança do Azure decidirá automaticamente um local para salvar alguns dos seus dados.</span><span class="sxs-lookup"><span data-stu-id="a6c27-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="a6c27-110">Use este cmdlet para descobrir esse local.</span><span class="sxs-lookup"><span data-stu-id="a6c27-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="a6c27-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6c27-111">EXAMPLES</span></span>

### <span data-ttu-id="a6c27-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a6c27-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="a6c27-113">Obtém o local onde o Centro de Segurança do Azure salva os dados de segurança calculados.</span><span class="sxs-lookup"><span data-stu-id="a6c27-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="a6c27-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a6c27-114">PARAMETERS</span></span>

### <span data-ttu-id="a6c27-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c27-115">-DefaultProfile</span></span>
<span data-ttu-id="a6c27-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c27-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6c27-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a6c27-117">-Name</span></span>
<span data-ttu-id="a6c27-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a6c27-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c27-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6c27-119">-ResourceId</span></span>
<span data-ttu-id="a6c27-120">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a6c27-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6c27-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c27-121">CommonParameters</span></span>
<span data-ttu-id="a6c27-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6c27-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c27-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6c27-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c27-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6c27-124">INPUTS</span></span>

### <span data-ttu-id="a6c27-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a6c27-125">System.String</span></span>

## <span data-ttu-id="a6c27-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a6c27-126">OUTPUTS</span></span>

### <span data-ttu-id="a6c27-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="a6c27-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="a6c27-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="a6c27-128">NOTES</span></span>

## <span data-ttu-id="a6c27-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6c27-129">RELATED LINKS</span></span>
