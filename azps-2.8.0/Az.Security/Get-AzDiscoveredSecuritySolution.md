---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: d5fca22bf289c42681d9af18a9eaff28587f1922
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773272"
---
# <span data-ttu-id="cfb61-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="cfb61-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="cfb61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cfb61-102">SYNOPSIS</span></span>
<span data-ttu-id="cfb61-103">Obtém soluções de segurança descobertas pela central de segurança do Azure</span><span class="sxs-lookup"><span data-stu-id="cfb61-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="cfb61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfb61-104">SYNTAX</span></span>

### <span data-ttu-id="cfb61-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="cfb61-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfb61-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="cfb61-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfb61-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="cfb61-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfb61-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cfb61-108">DESCRIPTION</span></span>
<span data-ttu-id="cfb61-109">As soluções de segurança são descobertas automaticamente pela central de segurança do Azure, use esse cmdlet para exibir as soluções de segurança descobertas</span><span class="sxs-lookup"><span data-stu-id="cfb61-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="cfb61-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cfb61-110">EXAMPLES</span></span>

### <span data-ttu-id="cfb61-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cfb61-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="cfb61-112">Obter todas as soluções de segurança descobertas na assinatura</span><span class="sxs-lookup"><span data-stu-id="cfb61-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="cfb61-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cfb61-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="cfb61-114">Obter uma solução específica de segurança descoberta</span><span class="sxs-lookup"><span data-stu-id="cfb61-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="cfb61-115">OS</span><span class="sxs-lookup"><span data-stu-id="cfb61-115">PARAMETERS</span></span>

### <span data-ttu-id="cfb61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfb61-116">-DefaultProfile</span></span>
<span data-ttu-id="cfb61-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cfb61-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfb61-118">-Local</span><span class="sxs-lookup"><span data-stu-id="cfb61-118">-Location</span></span>
<span data-ttu-id="cfb61-119">Ponto.</span><span class="sxs-lookup"><span data-stu-id="cfb61-119">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfb61-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="cfb61-120">-Name</span></span>
<span data-ttu-id="cfb61-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="cfb61-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfb61-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfb61-122">-ResourceGroupName</span></span>
<span data-ttu-id="cfb61-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cfb61-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfb61-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfb61-124">-ResourceId</span></span>
<span data-ttu-id="cfb61-125">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="cfb61-125">Resource ID.</span></span>

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

### <span data-ttu-id="cfb61-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfb61-126">CommonParameters</span></span>
<span data-ttu-id="cfb61-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfb61-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfb61-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfb61-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfb61-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cfb61-129">INPUTS</span></span>

### <span data-ttu-id="cfb61-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cfb61-130">System.String</span></span>

## <span data-ttu-id="cfb61-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cfb61-131">OUTPUTS</span></span>

### <span data-ttu-id="cfb61-132">Microsoft. Azure. Commands. Security. Models. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="cfb61-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="cfb61-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cfb61-133">NOTES</span></span>

## <span data-ttu-id="cfb61-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfb61-134">RELATED LINKS</span></span>