---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: c961ccc6bf02f7b28cf1cefd35ca27adb76bc14e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111391"
---
# <span data-ttu-id="08167-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="08167-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="08167-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08167-102">SYNOPSIS</span></span>
<span data-ttu-id="08167-103">Não registrou um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="08167-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="08167-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08167-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08167-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="08167-105">DESCRIPTION</span></span>
<span data-ttu-id="08167-106">O **cmdlet Unregister-AzProviderFeature** não registrou um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="08167-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="08167-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="08167-107">EXAMPLES</span></span>

### <span data-ttu-id="08167-108">Exemplo 1: Não registro de um recurso</span><span class="sxs-lookup"><span data-stu-id="08167-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="08167-109">Isso desinforma o recurso AllowApplicationSecurityGroups da Microsoft.Network de sua conta.</span><span class="sxs-lookup"><span data-stu-id="08167-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="08167-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08167-110">PARAMETERS</span></span>

### <span data-ttu-id="08167-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08167-111">-DefaultProfile</span></span>
<span data-ttu-id="08167-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="08167-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08167-113">-Nomedo Recurso</span><span class="sxs-lookup"><span data-stu-id="08167-113">-FeatureName</span></span>
<span data-ttu-id="08167-114">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="08167-114">The feature name.</span></span>

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

### <span data-ttu-id="08167-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="08167-115">-ProviderNamespace</span></span>
<span data-ttu-id="08167-116">O namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="08167-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="08167-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="08167-117">-Confirm</span></span>
<span data-ttu-id="08167-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08167-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08167-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08167-119">-WhatIf</span></span>
<span data-ttu-id="08167-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="08167-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08167-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08167-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08167-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08167-122">CommonParameters</span></span>
<span data-ttu-id="08167-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08167-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08167-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08167-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08167-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="08167-125">INPUTS</span></span>

### <span data-ttu-id="08167-126">System.String</span><span class="sxs-lookup"><span data-stu-id="08167-126">System.String</span></span>

## <span data-ttu-id="08167-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="08167-127">OUTPUTS</span></span>

### <span data-ttu-id="08167-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="08167-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="08167-129">Notas</span><span class="sxs-lookup"><span data-stu-id="08167-129">NOTES</span></span>

## <span data-ttu-id="08167-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08167-130">RELATED LINKS</span></span>