---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: c51cb2eaa00e870eee3e70e0e86c4da3fb36a330
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886315"
---
# <span data-ttu-id="093b1-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="093b1-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="093b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="093b1-102">SYNOPSIS</span></span>
<span data-ttu-id="093b1-103">Não registrou um provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="093b1-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="093b1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="093b1-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="093b1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="093b1-105">DESCRIPTION</span></span>
<span data-ttu-id="093b1-106">O **cmdlet Unregister-AzResourceProvider** não tem registro em um provedor de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="093b1-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="093b1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="093b1-107">EXAMPLES</span></span>

### <span data-ttu-id="093b1-108">Exemplo 1: provedor de recursos de registro sem registro com ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="093b1-108">Example 1: Unregister resource provider with ProviderNamespace</span></span>

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

<span data-ttu-id="093b1-109">Esse comando não registrou o provedor de recursos "Microsoft.support".</span><span class="sxs-lookup"><span data-stu-id="093b1-109">This command unregisters the resource provider "Microsoft.support".</span></span>

## <span data-ttu-id="093b1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="093b1-110">PARAMETERS</span></span>

### <span data-ttu-id="093b1-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="093b1-111">-ApiVersion</span></span>
<span data-ttu-id="093b1-112">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="093b1-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="093b1-113">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="093b1-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="093b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="093b1-114">-DefaultProfile</span></span>
<span data-ttu-id="093b1-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="093b1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="093b1-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="093b1-116">-Pre</span></span>
<span data-ttu-id="093b1-117">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="093b1-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="093b1-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="093b1-118">-ProviderNamespace</span></span>
<span data-ttu-id="093b1-119">Especifica o namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="093b1-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="093b1-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="093b1-120">-Confirm</span></span>
<span data-ttu-id="093b1-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="093b1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="093b1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="093b1-122">-WhatIf</span></span>
<span data-ttu-id="093b1-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="093b1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="093b1-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="093b1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="093b1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="093b1-125">CommonParameters</span></span>
<span data-ttu-id="093b1-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="093b1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="093b1-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="093b1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="093b1-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="093b1-128">INPUTS</span></span>

### <span data-ttu-id="093b1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="093b1-129">System.String</span></span>

## <span data-ttu-id="093b1-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="093b1-130">OUTPUTS</span></span>

### <span data-ttu-id="093b1-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="093b1-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="093b1-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="093b1-132">NOTES</span></span>

## <span data-ttu-id="093b1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="093b1-133">RELATED LINKS</span></span>

[<span data-ttu-id="093b1-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="093b1-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="093b1-135">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="093b1-135">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


