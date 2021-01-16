---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: c961ccc6bf02f7b28cf1cefd35ca27adb76bc14e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260223"
---
# <span data-ttu-id="fb57a-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="fb57a-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="fb57a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb57a-102">SYNOPSIS</span></span>
<span data-ttu-id="fb57a-103">Cancela o registro de um recurso de provedor do Azure na sua conta.</span><span class="sxs-lookup"><span data-stu-id="fb57a-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="fb57a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb57a-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb57a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb57a-105">DESCRIPTION</span></span>
<span data-ttu-id="fb57a-106">O cmdlet **Unregister-AzProviderFeature** cancela o registro de um recurso de provedor do Azure na sua conta.</span><span class="sxs-lookup"><span data-stu-id="fb57a-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="fb57a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb57a-107">EXAMPLES</span></span>

### <span data-ttu-id="fb57a-108">Exemplo 1: cancelar o registro de um recurso</span><span class="sxs-lookup"><span data-stu-id="fb57a-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="fb57a-109">Isso cancela o registro do recurso AllowApplicationSecurityGroups para Microsoft. Network da sua conta.</span><span class="sxs-lookup"><span data-stu-id="fb57a-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="fb57a-110">OS</span><span class="sxs-lookup"><span data-stu-id="fb57a-110">PARAMETERS</span></span>

### <span data-ttu-id="fb57a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb57a-111">-DefaultProfile</span></span>
<span data-ttu-id="fb57a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb57a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb57a-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="fb57a-113">-FeatureName</span></span>
<span data-ttu-id="fb57a-114">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="fb57a-114">The feature name.</span></span>

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

### <span data-ttu-id="fb57a-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="fb57a-115">-ProviderNamespace</span></span>
<span data-ttu-id="fb57a-116">O namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="fb57a-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="fb57a-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb57a-117">-Confirm</span></span>
<span data-ttu-id="fb57a-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb57a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb57a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb57a-119">-WhatIf</span></span>
<span data-ttu-id="fb57a-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb57a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb57a-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb57a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb57a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb57a-122">CommonParameters</span></span>
<span data-ttu-id="fb57a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb57a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb57a-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb57a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb57a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb57a-125">INPUTS</span></span>

### <span data-ttu-id="fb57a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fb57a-126">System.String</span></span>

## <span data-ttu-id="fb57a-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb57a-127">OUTPUTS</span></span>

### <span data-ttu-id="fb57a-128">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="fb57a-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="fb57a-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb57a-129">NOTES</span></span>

## <span data-ttu-id="fb57a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb57a-130">RELATED LINKS</span></span>