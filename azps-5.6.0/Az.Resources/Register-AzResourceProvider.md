---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 8fe856b1b8b710c1db139474f15d432f32c2652a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889167"
---
# <span data-ttu-id="4afe4-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4afe4-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="4afe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4afe4-102">SYNOPSIS</span></span>
<span data-ttu-id="4afe4-103">Registra um provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="4afe4-103">Registers a resource provider.</span></span>

## <span data-ttu-id="4afe4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4afe4-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4afe4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4afe4-105">DESCRIPTION</span></span>
<span data-ttu-id="4afe4-106">O cmdlet **Register-AzResourceProvider** registra um provedor de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4afe4-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="4afe4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4afe4-107">EXAMPLES</span></span>

### <span data-ttu-id="4afe4-108">Exemplo 1: Registrar um provedor</span><span class="sxs-lookup"><span data-stu-id="4afe4-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="4afe4-109">Isso registra o provedor Microsoft.Network para sua conta.</span><span class="sxs-lookup"><span data-stu-id="4afe4-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="4afe4-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4afe4-110">PARAMETERS</span></span>

### <span data-ttu-id="4afe4-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4afe4-111">-ApiVersion</span></span>
<span data-ttu-id="4afe4-112">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="4afe4-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4afe4-113">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="4afe4-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4afe4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4afe4-114">-DefaultProfile</span></span>
<span data-ttu-id="4afe4-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4afe4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4afe4-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="4afe4-116">-Pre</span></span>
<span data-ttu-id="4afe4-117">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="4afe4-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afe4-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="4afe4-118">-ProviderNamespace</span></span>
<span data-ttu-id="4afe4-119">Especifica o namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="4afe4-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="4afe4-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4afe4-120">-Confirm</span></span>
<span data-ttu-id="4afe4-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4afe4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4afe4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4afe4-122">-WhatIf</span></span>
<span data-ttu-id="4afe4-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4afe4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4afe4-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4afe4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4afe4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4afe4-125">CommonParameters</span></span>
<span data-ttu-id="4afe4-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4afe4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4afe4-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4afe4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4afe4-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4afe4-128">INPUTS</span></span>

### <span data-ttu-id="4afe4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4afe4-129">System.String</span></span>

## <span data-ttu-id="4afe4-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4afe4-130">OUTPUTS</span></span>

### <span data-ttu-id="4afe4-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4afe4-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="4afe4-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="4afe4-132">NOTES</span></span>

## <span data-ttu-id="4afe4-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4afe4-133">RELATED LINKS</span></span>

[<span data-ttu-id="4afe4-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4afe4-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="4afe4-135">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4afe4-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


