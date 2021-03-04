---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 1ab198fc422cfb0f880f8c1a3dcd860134b4c2c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901580"
---
# <span data-ttu-id="5cc08-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="5cc08-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="5cc08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cc08-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc08-103">Registra um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="5cc08-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="5cc08-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5cc08-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cc08-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5cc08-105">DESCRIPTION</span></span>
<span data-ttu-id="5cc08-106">O cmdlet **Register-AzProviderFeature** registra um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="5cc08-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="5cc08-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5cc08-107">EXAMPLES</span></span>

### <span data-ttu-id="5cc08-108">Exemplo 1: Registrar um recurso</span><span class="sxs-lookup"><span data-stu-id="5cc08-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="5cc08-109">Isso adiciona o recurso AllowApplicationSecurityGroups para Microsoft.Network à sua conta.</span><span class="sxs-lookup"><span data-stu-id="5cc08-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="5cc08-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5cc08-110">PARAMETERS</span></span>

### <span data-ttu-id="5cc08-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cc08-111">-DefaultProfile</span></span>
<span data-ttu-id="5cc08-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5cc08-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cc08-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="5cc08-113">-FeatureName</span></span>
<span data-ttu-id="5cc08-114">Especifica o nome do recurso que esse cmdlet registra.</span><span class="sxs-lookup"><span data-stu-id="5cc08-114">Specifies the name of the feature that this cmdlet registers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cc08-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="5cc08-115">-ProviderNamespace</span></span>
<span data-ttu-id="5cc08-116">Especifica um namespace para o qual esse cmdlet registra um recurso de provedor.</span><span class="sxs-lookup"><span data-stu-id="5cc08-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cc08-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cc08-117">-Confirm</span></span>
<span data-ttu-id="5cc08-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cc08-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc08-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cc08-119">-WhatIf</span></span>
<span data-ttu-id="5cc08-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5cc08-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cc08-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5cc08-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc08-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc08-122">CommonParameters</span></span>
<span data-ttu-id="5cc08-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cc08-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc08-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cc08-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc08-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cc08-125">INPUTS</span></span>

### <span data-ttu-id="5cc08-126">System.String</span><span class="sxs-lookup"><span data-stu-id="5cc08-126">System.String</span></span>

## <span data-ttu-id="5cc08-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5cc08-127">OUTPUTS</span></span>

### <span data-ttu-id="5cc08-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="5cc08-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="5cc08-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="5cc08-129">NOTES</span></span>

## <span data-ttu-id="5cc08-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5cc08-130">RELATED LINKS</span></span>

[<span data-ttu-id="5cc08-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="5cc08-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


