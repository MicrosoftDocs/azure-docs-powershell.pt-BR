---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: f79b3b4e8347c485230141416461c1f320d3d7b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891224"
---
# <span data-ttu-id="298ca-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="298ca-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="298ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="298ca-102">SYNOPSIS</span></span>
<span data-ttu-id="298ca-103">Obtém um grupo de origem da CDN</span><span class="sxs-lookup"><span data-stu-id="298ca-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="298ca-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="298ca-104">SYNTAX</span></span>

### <span data-ttu-id="298ca-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="298ca-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="298ca-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="298ca-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="298ca-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="298ca-107">DESCRIPTION</span></span>
<span data-ttu-id="298ca-108">O Get-AzCdnOriginGroup cmdlet recupera um grupo de origem da CDN.</span><span class="sxs-lookup"><span data-stu-id="298ca-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="298ca-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="298ca-109">EXAMPLES</span></span>

### <span data-ttu-id="298ca-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="298ca-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="298ca-111">Este comando obterá o grupo de origem dentro do ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="298ca-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="298ca-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="298ca-112">PARAMETERS</span></span>

### <span data-ttu-id="298ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="298ca-113">-DefaultProfile</span></span>
<span data-ttu-id="298ca-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="298ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="298ca-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="298ca-115">-EndpointName</span></span>
<span data-ttu-id="298ca-116">Nome do ponto de extremidade cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="298ca-116">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="298ca-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="298ca-117">-OriginGroupName</span></span>
<span data-ttu-id="298ca-118">Nome do grupo de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="298ca-118">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="298ca-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="298ca-119">-ProfileName</span></span>
<span data-ttu-id="298ca-120">Nome do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="298ca-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="298ca-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="298ca-121">-ResourceGroupName</span></span>
<span data-ttu-id="298ca-122">O grupo de recursos do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="298ca-122">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="298ca-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="298ca-123">-ResourceId</span></span>
<span data-ttu-id="298ca-124">ID do recurso para o grupo de origem</span><span class="sxs-lookup"><span data-stu-id="298ca-124">Resource Id for the the origin group</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="298ca-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="298ca-125">CommonParameters</span></span>
<span data-ttu-id="298ca-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="298ca-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="298ca-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="298ca-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="298ca-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="298ca-128">INPUTS</span></span>

### <span data-ttu-id="298ca-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="298ca-129">None</span></span>

## <span data-ttu-id="298ca-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="298ca-130">OUTPUTS</span></span>

### <span data-ttu-id="298ca-131">System.Object</span><span class="sxs-lookup"><span data-stu-id="298ca-131">System.Object</span></span>

## <span data-ttu-id="298ca-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="298ca-132">NOTES</span></span>

## <span data-ttu-id="298ca-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="298ca-133">RELATED LINKS</span></span>
