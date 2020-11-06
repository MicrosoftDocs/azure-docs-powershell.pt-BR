---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
ms.openlocfilehash: 034681ad8ce4fbd30b10b959eda024f1a375c366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427163"
---
# <span data-ttu-id="29e6d-101">Get-AzureRmSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="29e6d-101">Get-AzureRmSecurityLocation</span></span>

## <span data-ttu-id="29e6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="29e6d-103">Obtém o local onde a central de segurança do Azure salvará automaticamente os dados para a assinatura específica</span><span class="sxs-lookup"><span data-stu-id="29e6d-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29e6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29e6d-104">SYNTAX</span></span>

### <span data-ttu-id="29e6d-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="29e6d-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29e6d-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="29e6d-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29e6d-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="29e6d-107">ResourceId</span></span>
```
Get-AzureRmSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29e6d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29e6d-108">DESCRIPTION</span></span>
<span data-ttu-id="29e6d-109">A central de segurança do Azure decidirá automaticamente um local para salvar alguns dos seus dados.</span><span class="sxs-lookup"><span data-stu-id="29e6d-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="29e6d-110">Use esse cmdlet para descobrir esse local.</span><span class="sxs-lookup"><span data-stu-id="29e6d-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="29e6d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29e6d-111">EXAMPLES</span></span>

### <span data-ttu-id="29e6d-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29e6d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="29e6d-113">Obtém o local onde a central de segurança do Azure salva os dados de segurança calculados.</span><span class="sxs-lookup"><span data-stu-id="29e6d-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="29e6d-114">OS</span><span class="sxs-lookup"><span data-stu-id="29e6d-114">PARAMETERS</span></span>

### <span data-ttu-id="29e6d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e6d-115">-DefaultProfile</span></span>
<span data-ttu-id="29e6d-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29e6d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29e6d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="29e6d-117">-Name</span></span>
<span data-ttu-id="29e6d-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="29e6d-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e6d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29e6d-119">-ResourceId</span></span>
<span data-ttu-id="29e6d-120">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="29e6d-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e6d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e6d-121">CommonParameters</span></span>
<span data-ttu-id="29e6d-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29e6d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e6d-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29e6d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e6d-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29e6d-124">INPUTS</span></span>

### <span data-ttu-id="29e6d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="29e6d-125">System.String</span></span>

## <span data-ttu-id="29e6d-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29e6d-126">OUTPUTS</span></span>

### <span data-ttu-id="29e6d-127">Microsoft. Azure. Commands. Security. Models. Locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="29e6d-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="29e6d-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29e6d-128">NOTES</span></span>

## <span data-ttu-id="29e6d-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29e6d-129">RELATED LINKS</span></span>
