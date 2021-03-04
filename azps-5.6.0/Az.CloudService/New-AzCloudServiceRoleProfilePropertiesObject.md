---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceRoleProfilePropertiesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
ms.openlocfilehash: 6eec8f849d555fd2bf71f564c2e5c3ed9c699d80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888736"
---
# <span data-ttu-id="b8000-101">New-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="b8000-101">New-AzCloudServiceRoleProfilePropertiesObject</span></span>

## <span data-ttu-id="b8000-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8000-102">SYNOPSIS</span></span>
<span data-ttu-id="b8000-103">Criar um objeto na memória para CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="b8000-103">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="b8000-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b8000-104">SYNTAX</span></span>

```
New-AzCloudServiceRoleProfilePropertiesObject [-Name <String>] [-SkuCapacity <Int64>] [-SkuName <String>]
 [-SkuTier <String>] [<CommonParameters>]
```

## <span data-ttu-id="b8000-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b8000-105">DESCRIPTION</span></span>
<span data-ttu-id="b8000-106">Criar um objeto na memória para CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="b8000-106">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="b8000-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8000-107">EXAMPLES</span></span>

### <span data-ttu-id="b8000-108">Exemplo 1: Criar objeto de propriedades de perfil de função</span><span class="sxs-lookup"><span data-stu-id="b8000-108">Example 1: Create role profile properties object</span></span>
```powershell
$role = New-AzCloudServiceRoleProfilePropertiesObject -Name 'WebRole' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
```

<span data-ttu-id="b8000-109">Este comando cria um objeto de propriedades de perfil de função que é usado para criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b8000-109">This command creates role profile properties object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="b8000-110">Para obter mais detalhes, consulte New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="b8000-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="b8000-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b8000-111">PARAMETERS</span></span>

### <span data-ttu-id="b8000-112">-Name</span><span class="sxs-lookup"><span data-stu-id="b8000-112">-Name</span></span>
<span data-ttu-id="b8000-113">Nome do perfil de função.</span><span class="sxs-lookup"><span data-stu-id="b8000-113">Name of role profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8000-114">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b8000-114">-SkuCapacity</span></span>
<span data-ttu-id="b8000-115">Especifica o número de instâncias de função no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b8000-115">Specifies the number of role instances in the cloud service.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8000-116">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b8000-116">-SkuName</span></span>
<span data-ttu-id="b8000-117">O nome sku.</span><span class="sxs-lookup"><span data-stu-id="b8000-117">The sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8000-118">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b8000-118">-SkuTier</span></span>
<span data-ttu-id="b8000-119">SkuTier.</span><span class="sxs-lookup"><span data-stu-id="b8000-119">SkuTier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8000-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8000-120">CommonParameters</span></span>
<span data-ttu-id="b8000-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8000-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8000-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8000-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8000-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8000-123">INPUTS</span></span>

## <span data-ttu-id="b8000-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b8000-124">OUTPUTS</span></span>

### <span data-ttu-id="b8000-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="b8000-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="b8000-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="b8000-126">NOTES</span></span>

<span data-ttu-id="b8000-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b8000-127">ALIASES</span></span>

## <span data-ttu-id="b8000-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8000-128">RELATED LINKS</span></span>

