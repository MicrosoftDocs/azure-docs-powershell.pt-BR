---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceRoleProfilePropertiesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
ms.openlocfilehash: c9e41a6a4fa7a89db31304dc343da466e8632a74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112164"
---
# <span data-ttu-id="53f9c-101">New-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="53f9c-101">New-AzCloudServiceRoleProfilePropertiesObject</span></span>

## <span data-ttu-id="53f9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="53f9c-103">Criar um objeto na memória para CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="53f9c-103">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="53f9c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53f9c-104">SYNTAX</span></span>

```
New-AzCloudServiceRoleProfilePropertiesObject [-Name <String>] [-SkuCapacity <Int64>] [-SkuName <String>]
 [-SkuTier <String>] [<CommonParameters>]
```

## <span data-ttu-id="53f9c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="53f9c-105">DESCRIPTION</span></span>
<span data-ttu-id="53f9c-106">Criar um objeto na memória para CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="53f9c-106">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="53f9c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="53f9c-107">EXAMPLES</span></span>

### <span data-ttu-id="53f9c-108">Exemplo 1: Criar objeto de propriedades de perfil de função</span><span class="sxs-lookup"><span data-stu-id="53f9c-108">Example 1: Create role profile properties object</span></span>
```powershell
$role = New-AzCloudServiceRoleProfilePropertiesObject -Name 'WebRole' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
```

<span data-ttu-id="53f9c-109">Esse comando cria um objeto de propriedades de perfil de função que é usado para criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="53f9c-109">This command creates role profile properties object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="53f9c-110">Para obter mais detalhes, consulte New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="53f9c-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="53f9c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53f9c-111">PARAMETERS</span></span>

### <span data-ttu-id="53f9c-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="53f9c-112">-Name</span></span>
<span data-ttu-id="53f9c-113">Nome do perfil da função.</span><span class="sxs-lookup"><span data-stu-id="53f9c-113">Name of role profile.</span></span>

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

### <span data-ttu-id="53f9c-114">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="53f9c-114">-SkuCapacity</span></span>
<span data-ttu-id="53f9c-115">Especifica o número de instâncias de função no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="53f9c-115">Specifies the number of role instances in the cloud service.</span></span>

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

### <span data-ttu-id="53f9c-116">-SkuName</span><span class="sxs-lookup"><span data-stu-id="53f9c-116">-SkuName</span></span>
<span data-ttu-id="53f9c-117">O nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="53f9c-117">The sku name.</span></span>

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

### <span data-ttu-id="53f9c-118">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="53f9c-118">-SkuTier</span></span>
<span data-ttu-id="53f9c-119">SkuTier.</span><span class="sxs-lookup"><span data-stu-id="53f9c-119">SkuTier.</span></span>

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

### <span data-ttu-id="53f9c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f9c-120">CommonParameters</span></span>
<span data-ttu-id="53f9c-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53f9c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f9c-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53f9c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f9c-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="53f9c-123">INPUTS</span></span>

## <span data-ttu-id="53f9c-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="53f9c-124">OUTPUTS</span></span>

### <span data-ttu-id="53f9c-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="53f9c-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="53f9c-126">Notas</span><span class="sxs-lookup"><span data-stu-id="53f9c-126">NOTES</span></span>

<span data-ttu-id="53f9c-127">Aliases</span><span class="sxs-lookup"><span data-stu-id="53f9c-127">ALIASES</span></span>

## <span data-ttu-id="53f9c-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53f9c-128">RELATED LINKS</span></span>

