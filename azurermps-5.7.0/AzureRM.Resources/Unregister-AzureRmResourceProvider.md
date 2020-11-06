---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/unregister-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
ms.openlocfilehash: 875dd42cb0aefd6d6422d99463cd56ace720411a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603220"
---
# <span data-ttu-id="5954e-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5954e-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="5954e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5954e-102">SYNOPSIS</span></span>
<span data-ttu-id="5954e-103">Cancela o registro de um provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="5954e-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5954e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5954e-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5954e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5954e-105">DESCRIPTION</span></span>
<span data-ttu-id="5954e-106">O cmdlet **Unregister-AzureRmResourceProvider** cancela o registro de um provedor de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5954e-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="5954e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5954e-107">EXAMPLES</span></span>

## <span data-ttu-id="5954e-108">OS</span><span class="sxs-lookup"><span data-stu-id="5954e-108">PARAMETERS</span></span>

### <span data-ttu-id="5954e-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5954e-109">-ApiVersion</span></span>
<span data-ttu-id="5954e-110">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="5954e-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5954e-111">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="5954e-111">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5954e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5954e-112">-DefaultProfile</span></span>
<span data-ttu-id="5954e-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5954e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5954e-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="5954e-114">-Pre</span></span>
<span data-ttu-id="5954e-115">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="5954e-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5954e-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="5954e-116">-ProviderNamespace</span></span>
<span data-ttu-id="5954e-117">Especifica o namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="5954e-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="5954e-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5954e-118">-Confirm</span></span>
<span data-ttu-id="5954e-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5954e-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5954e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5954e-120">-WhatIf</span></span>
<span data-ttu-id="5954e-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5954e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5954e-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5954e-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5954e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5954e-123">CommonParameters</span></span>
<span data-ttu-id="5954e-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5954e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5954e-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5954e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5954e-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5954e-126">INPUTS</span></span>

### <span data-ttu-id="5954e-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5954e-127">None</span></span>
<span data-ttu-id="5954e-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5954e-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5954e-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5954e-129">OUTPUTS</span></span>

### <span data-ttu-id="5954e-130">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceProvider]</span><span class="sxs-lookup"><span data-stu-id="5954e-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider]</span></span>

## <span data-ttu-id="5954e-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5954e-131">NOTES</span></span>

## <span data-ttu-id="5954e-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5954e-132">RELATED LINKS</span></span>

[<span data-ttu-id="5954e-133">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5954e-133">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="5954e-134">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5954e-134">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


