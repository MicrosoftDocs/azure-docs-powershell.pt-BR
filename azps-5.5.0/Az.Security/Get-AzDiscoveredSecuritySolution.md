---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: 1fbe9e790966a92c38ba79b56221e5e6083b649c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116207"
---
# <span data-ttu-id="7581e-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="7581e-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="7581e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7581e-102">SYNOPSIS</span></span>
<span data-ttu-id="7581e-103">Obtém soluções de segurança que foram descobertas pela Central de Segurança do Azure</span><span class="sxs-lookup"><span data-stu-id="7581e-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="7581e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7581e-104">SYNTAX</span></span>

### <span data-ttu-id="7581e-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7581e-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7581e-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="7581e-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7581e-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="7581e-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7581e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7581e-108">DESCRIPTION</span></span>
<span data-ttu-id="7581e-109">As soluções de segurança são descobertas automaticamente pela Central de Segurança do Azure, use este cmdlet para exibir as soluções de segurança descobertas</span><span class="sxs-lookup"><span data-stu-id="7581e-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="7581e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7581e-110">EXAMPLES</span></span>

### <span data-ttu-id="7581e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7581e-111">Example 1</span></span>
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

<span data-ttu-id="7581e-112">Obter todas as soluções de segurança descobertas na assinatura</span><span class="sxs-lookup"><span data-stu-id="7581e-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="7581e-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7581e-113">Example 2</span></span>
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

<span data-ttu-id="7581e-114">Obter uma solução de segurança descoberta específica</span><span class="sxs-lookup"><span data-stu-id="7581e-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="7581e-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7581e-115">PARAMETERS</span></span>

### <span data-ttu-id="7581e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7581e-116">-DefaultProfile</span></span>
<span data-ttu-id="7581e-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7581e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7581e-118">-Local</span><span class="sxs-lookup"><span data-stu-id="7581e-118">-Location</span></span>
<span data-ttu-id="7581e-119">Localização.</span><span class="sxs-lookup"><span data-stu-id="7581e-119">Location.</span></span>

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

### <span data-ttu-id="7581e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7581e-120">-Name</span></span>
<span data-ttu-id="7581e-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="7581e-121">Resource name.</span></span>

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

### <span data-ttu-id="7581e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7581e-122">-ResourceGroupName</span></span>
<span data-ttu-id="7581e-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7581e-123">Resource group name.</span></span>

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

### <span data-ttu-id="7581e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7581e-124">-ResourceId</span></span>
<span data-ttu-id="7581e-125">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="7581e-125">Resource ID.</span></span>

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

### <span data-ttu-id="7581e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7581e-126">CommonParameters</span></span>
<span data-ttu-id="7581e-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7581e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7581e-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7581e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7581e-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="7581e-129">INPUTS</span></span>

### <span data-ttu-id="7581e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7581e-130">System.String</span></span>

## <span data-ttu-id="7581e-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="7581e-131">OUTPUTS</span></span>

### <span data-ttu-id="7581e-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="7581e-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="7581e-133">Notas</span><span class="sxs-lookup"><span data-stu-id="7581e-133">NOTES</span></span>

## <span data-ttu-id="7581e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7581e-134">RELATED LINKS</span></span>
