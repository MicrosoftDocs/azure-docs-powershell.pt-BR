---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 35cb8ad956419a2fcbfe427ce23e518986da63ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118743"
---
# <span data-ttu-id="e6017-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="e6017-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="e6017-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6017-102">SYNOPSIS</span></span>
<span data-ttu-id="e6017-103">Registra um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="e6017-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="e6017-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6017-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6017-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6017-105">DESCRIPTION</span></span>
<span data-ttu-id="e6017-106">O cmdlet **Register-AzProviderFeature** registra um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="e6017-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="e6017-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e6017-107">EXAMPLES</span></span>

### <span data-ttu-id="e6017-108">Exemplo 1: Registrar um recurso</span><span class="sxs-lookup"><span data-stu-id="e6017-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="e6017-109">Isso adiciona o recurso AllowApplicationSecurityGroups para Microsoft.Network à sua conta.</span><span class="sxs-lookup"><span data-stu-id="e6017-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="e6017-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6017-110">PARAMETERS</span></span>

### <span data-ttu-id="e6017-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6017-111">-DefaultProfile</span></span>
<span data-ttu-id="e6017-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e6017-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6017-113">-Nomedo Recurso</span><span class="sxs-lookup"><span data-stu-id="e6017-113">-FeatureName</span></span>
<span data-ttu-id="e6017-114">Especifica o nome do recurso que esse cmdlet registra.</span><span class="sxs-lookup"><span data-stu-id="e6017-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="e6017-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="e6017-115">-ProviderNamespace</span></span>
<span data-ttu-id="e6017-116">Especifica um namespace para o qual este cmdlet registra um recurso de provedor.</span><span class="sxs-lookup"><span data-stu-id="e6017-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="e6017-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e6017-117">-Confirm</span></span>
<span data-ttu-id="e6017-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6017-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6017-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6017-119">-WhatIf</span></span>
<span data-ttu-id="e6017-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e6017-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6017-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e6017-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6017-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6017-122">CommonParameters</span></span>
<span data-ttu-id="e6017-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6017-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6017-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6017-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6017-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="e6017-125">INPUTS</span></span>

### <span data-ttu-id="e6017-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e6017-126">System.String</span></span>

## <span data-ttu-id="e6017-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="e6017-127">OUTPUTS</span></span>

### <span data-ttu-id="e6017-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="e6017-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="e6017-129">Notas</span><span class="sxs-lookup"><span data-stu-id="e6017-129">NOTES</span></span>

## <span data-ttu-id="e6017-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6017-130">RELATED LINKS</span></span>

[<span data-ttu-id="e6017-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="e6017-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


