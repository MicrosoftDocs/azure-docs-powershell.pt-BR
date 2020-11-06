---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
ms.openlocfilehash: ecea7ba6aa34df73de65a4d03e004531e81ff497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429350"
---
# <span data-ttu-id="193bb-101">Get-AzureRmDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="193bb-101">Get-AzureRmDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="193bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="193bb-102">SYNOPSIS</span></span>
<span data-ttu-id="193bb-103">Obtém soluções de segurança descobertas pela central de segurança do Azure</span><span class="sxs-lookup"><span data-stu-id="193bb-103">Gets security solutions that were discovered by Azure Security Center</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="193bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="193bb-104">SYNTAX</span></span>

### <span data-ttu-id="193bb-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="193bb-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="193bb-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="193bb-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="193bb-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="193bb-107">ResourceId</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="193bb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="193bb-108">DESCRIPTION</span></span>
<span data-ttu-id="193bb-109">As soluções de segurança são descobertas automaticamente pela central de segurança do Azure, use esse cmdlet para exibir as soluções de segurança descobertas</span><span class="sxs-lookup"><span data-stu-id="193bb-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="193bb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="193bb-110">EXAMPLES</span></span>

### <span data-ttu-id="193bb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="193bb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="193bb-112">Obter todas as soluções de segurança descobertas na assinatura</span><span class="sxs-lookup"><span data-stu-id="193bb-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="193bb-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="193bb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="193bb-114">Obter uma solução específica de segurança descoberta</span><span class="sxs-lookup"><span data-stu-id="193bb-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="193bb-115">OS</span><span class="sxs-lookup"><span data-stu-id="193bb-115">PARAMETERS</span></span>

### <span data-ttu-id="193bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="193bb-116">-DefaultProfile</span></span>
<span data-ttu-id="193bb-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="193bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="193bb-118">-Local</span><span class="sxs-lookup"><span data-stu-id="193bb-118">-Location</span></span>
<span data-ttu-id="193bb-119">Ponto.</span><span class="sxs-lookup"><span data-stu-id="193bb-119">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="193bb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="193bb-120">-Name</span></span>
<span data-ttu-id="193bb-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="193bb-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="193bb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="193bb-122">-ResourceGroupName</span></span>
<span data-ttu-id="193bb-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="193bb-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="193bb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="193bb-124">-ResourceId</span></span>
<span data-ttu-id="193bb-125">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="193bb-125">Resource ID.</span></span>

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

### <span data-ttu-id="193bb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="193bb-126">CommonParameters</span></span>
<span data-ttu-id="193bb-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="193bb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="193bb-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="193bb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="193bb-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="193bb-129">INPUTS</span></span>

### <span data-ttu-id="193bb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="193bb-130">System.String</span></span>

## <span data-ttu-id="193bb-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="193bb-131">OUTPUTS</span></span>

### <span data-ttu-id="193bb-132">Microsoft. Azure. Commands. Security. Models. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="193bb-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="193bb-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="193bb-133">NOTES</span></span>

## <span data-ttu-id="193bb-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="193bb-134">RELATED LINKS</span></span>
