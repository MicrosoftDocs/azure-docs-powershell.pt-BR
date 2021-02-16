---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117912"
---
# <span data-ttu-id="235f9-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="235f9-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="235f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="235f9-102">SYNOPSIS</span></span>
<span data-ttu-id="235f9-103">Obtém um grupo de origem de CDN</span><span class="sxs-lookup"><span data-stu-id="235f9-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="235f9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="235f9-104">SYNTAX</span></span>

### <span data-ttu-id="235f9-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="235f9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="235f9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="235f9-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="235f9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="235f9-107">DESCRIPTION</span></span>
<span data-ttu-id="235f9-108">O cmdlet Get-AzCdnOriginGroup recupera um grupo de origem de CDN.</span><span class="sxs-lookup"><span data-stu-id="235f9-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="235f9-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="235f9-109">EXAMPLES</span></span>

### <span data-ttu-id="235f9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="235f9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="235f9-111">Esse comando obterá o grupo de origem dentro do ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="235f9-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="235f9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="235f9-112">PARAMETERS</span></span>

### <span data-ttu-id="235f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="235f9-113">-DefaultProfile</span></span>
<span data-ttu-id="235f9-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="235f9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="235f9-115">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="235f9-115">-EndpointName</span></span>
<span data-ttu-id="235f9-116">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="235f9-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="235f9-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="235f9-117">-OriginGroupName</span></span>
<span data-ttu-id="235f9-118">Nome do grupo de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="235f9-118">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="235f9-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="235f9-119">-ProfileName</span></span>
<span data-ttu-id="235f9-120">Nome de perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="235f9-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="235f9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="235f9-121">-ResourceGroupName</span></span>
<span data-ttu-id="235f9-122">O grupo de recursos do perfil de CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="235f9-122">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="235f9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="235f9-123">-ResourceId</span></span>
<span data-ttu-id="235f9-124">ID do Recurso do grupo de origem</span><span class="sxs-lookup"><span data-stu-id="235f9-124">Resource Id for the the origin group</span></span>

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

### <span data-ttu-id="235f9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="235f9-125">CommonParameters</span></span>
<span data-ttu-id="235f9-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="235f9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="235f9-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="235f9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="235f9-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="235f9-128">INPUTS</span></span>

### <span data-ttu-id="235f9-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="235f9-129">None</span></span>

## <span data-ttu-id="235f9-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="235f9-130">OUTPUTS</span></span>

### <span data-ttu-id="235f9-131">System.Object</span><span class="sxs-lookup"><span data-stu-id="235f9-131">System.Object</span></span>

## <span data-ttu-id="235f9-132">Notas</span><span class="sxs-lookup"><span data-stu-id="235f9-132">NOTES</span></span>

## <span data-ttu-id="235f9-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="235f9-133">RELATED LINKS</span></span>
