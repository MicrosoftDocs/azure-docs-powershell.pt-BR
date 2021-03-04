---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: 30c315240cf667db37c6c605cda093fe7811a3ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886319"
---
# <span data-ttu-id="0c07d-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="0c07d-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="0c07d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c07d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c07d-103">Não registrou um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="0c07d-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="0c07d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0c07d-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c07d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0c07d-105">DESCRIPTION</span></span>
<span data-ttu-id="0c07d-106">O **cmdlet Unregister-AzProviderFeature** não registrou um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="0c07d-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="0c07d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c07d-107">EXAMPLES</span></span>

### <span data-ttu-id="0c07d-108">Exemplo 1: Não registro de um recurso</span><span class="sxs-lookup"><span data-stu-id="0c07d-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="0c07d-109">Isso não faz o registro do recurso AllowApplicationSecurityGroups para Microsoft.Network de sua conta.</span><span class="sxs-lookup"><span data-stu-id="0c07d-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="0c07d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0c07d-110">PARAMETERS</span></span>

### <span data-ttu-id="0c07d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c07d-111">-DefaultProfile</span></span>
<span data-ttu-id="0c07d-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c07d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c07d-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="0c07d-113">-FeatureName</span></span>
<span data-ttu-id="0c07d-114">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0c07d-114">The feature name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c07d-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="0c07d-115">-ProviderNamespace</span></span>
<span data-ttu-id="0c07d-116">O namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c07d-116">The resource provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c07d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c07d-117">-Confirm</span></span>
<span data-ttu-id="0c07d-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c07d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c07d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c07d-119">-WhatIf</span></span>
<span data-ttu-id="0c07d-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0c07d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c07d-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0c07d-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c07d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c07d-122">CommonParameters</span></span>
<span data-ttu-id="0c07d-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c07d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c07d-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c07d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c07d-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c07d-125">INPUTS</span></span>

### <span data-ttu-id="0c07d-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0c07d-126">System.String</span></span>

## <span data-ttu-id="0c07d-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0c07d-127">OUTPUTS</span></span>

### <span data-ttu-id="0c07d-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="0c07d-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="0c07d-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="0c07d-129">NOTES</span></span>

## <span data-ttu-id="0c07d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c07d-130">RELATED LINKS</span></span>