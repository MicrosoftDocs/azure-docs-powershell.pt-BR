---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263278"
---
# <span data-ttu-id="88559-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="88559-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="88559-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88559-102">SYNOPSIS</span></span>
<span data-ttu-id="88559-103">Obtém um grupo de origem CDN</span><span class="sxs-lookup"><span data-stu-id="88559-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="88559-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88559-104">SYNTAX</span></span>

### <span data-ttu-id="88559-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="88559-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88559-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88559-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88559-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88559-107">DESCRIPTION</span></span>
<span data-ttu-id="88559-108">O cmdlet Get-AzCdnOriginGroup recupera um grupo de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="88559-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="88559-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88559-109">EXAMPLES</span></span>

### <span data-ttu-id="88559-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="88559-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="88559-111">Esse comando obterá o grupo de origem dentro do ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="88559-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="88559-112">OS</span><span class="sxs-lookup"><span data-stu-id="88559-112">PARAMETERS</span></span>

### <span data-ttu-id="88559-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88559-113">-DefaultProfile</span></span>
<span data-ttu-id="88559-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88559-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88559-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="88559-115">-EndpointName</span></span>
<span data-ttu-id="88559-116">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="88559-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="88559-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="88559-117">-OriginGroupName</span></span>
<span data-ttu-id="88559-118">Nome do grupo de origens da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="88559-118">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="88559-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="88559-119">-ProfileName</span></span>
<span data-ttu-id="88559-120">Nome do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="88559-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="88559-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88559-121">-ResourceGroupName</span></span>
<span data-ttu-id="88559-122">O grupo de recursos do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="88559-122">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="88559-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88559-123">-ResourceId</span></span>
<span data-ttu-id="88559-124">ID do recurso para o grupo de origem</span><span class="sxs-lookup"><span data-stu-id="88559-124">Resource Id for the the origin group</span></span>

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

### <span data-ttu-id="88559-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88559-125">CommonParameters</span></span>
<span data-ttu-id="88559-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88559-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88559-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88559-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88559-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88559-128">INPUTS</span></span>

### <span data-ttu-id="88559-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="88559-129">None</span></span>

## <span data-ttu-id="88559-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88559-130">OUTPUTS</span></span>

### <span data-ttu-id="88559-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="88559-131">System.Object</span></span>

## <span data-ttu-id="88559-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88559-132">NOTES</span></span>

## <span data-ttu-id="88559-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88559-133">RELATED LINKS</span></span>
