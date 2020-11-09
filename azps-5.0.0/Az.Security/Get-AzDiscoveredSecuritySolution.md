---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: 1fbe9e790966a92c38ba79b56221e5e6083b649c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281721"
---
# <span data-ttu-id="7ea18-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="7ea18-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="7ea18-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ea18-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea18-103">Obtém soluções de segurança descobertas pela central de segurança do Azure</span><span class="sxs-lookup"><span data-stu-id="7ea18-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="7ea18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ea18-104">SYNTAX</span></span>

### <span data-ttu-id="7ea18-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="7ea18-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ea18-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="7ea18-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ea18-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="7ea18-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ea18-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ea18-108">DESCRIPTION</span></span>
<span data-ttu-id="7ea18-109">As soluções de segurança são descobertas automaticamente pela central de segurança do Azure, use esse cmdlet para exibir as soluções de segurança descobertas</span><span class="sxs-lookup"><span data-stu-id="7ea18-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="7ea18-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ea18-110">EXAMPLES</span></span>

### <span data-ttu-id="7ea18-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ea18-111">Example 1</span></span>
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

<span data-ttu-id="7ea18-112">Obter todas as soluções de segurança descobertas na assinatura</span><span class="sxs-lookup"><span data-stu-id="7ea18-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="7ea18-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7ea18-113">Example 2</span></span>
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

<span data-ttu-id="7ea18-114">Obter uma solução específica de segurança descoberta</span><span class="sxs-lookup"><span data-stu-id="7ea18-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="7ea18-115">OS</span><span class="sxs-lookup"><span data-stu-id="7ea18-115">PARAMETERS</span></span>

### <span data-ttu-id="7ea18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea18-116">-DefaultProfile</span></span>
<span data-ttu-id="7ea18-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea18-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ea18-118">-Local</span><span class="sxs-lookup"><span data-stu-id="7ea18-118">-Location</span></span>
<span data-ttu-id="7ea18-119">Ponto.</span><span class="sxs-lookup"><span data-stu-id="7ea18-119">Location.</span></span>

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

### <span data-ttu-id="7ea18-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ea18-120">-Name</span></span>
<span data-ttu-id="7ea18-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="7ea18-121">Resource name.</span></span>

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

### <span data-ttu-id="7ea18-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea18-122">-ResourceGroupName</span></span>
<span data-ttu-id="7ea18-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7ea18-123">Resource group name.</span></span>

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

### <span data-ttu-id="7ea18-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ea18-124">-ResourceId</span></span>
<span data-ttu-id="7ea18-125">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="7ea18-125">Resource ID.</span></span>

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

### <span data-ttu-id="7ea18-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea18-126">CommonParameters</span></span>
<span data-ttu-id="7ea18-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ea18-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea18-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ea18-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea18-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ea18-129">INPUTS</span></span>

### <span data-ttu-id="7ea18-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7ea18-130">System.String</span></span>

## <span data-ttu-id="7ea18-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ea18-131">OUTPUTS</span></span>

### <span data-ttu-id="7ea18-132">Microsoft. Azure. Commands. Security. Models. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="7ea18-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="7ea18-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ea18-133">NOTES</span></span>

## <span data-ttu-id="7ea18-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ea18-134">RELATED LINKS</span></span>
