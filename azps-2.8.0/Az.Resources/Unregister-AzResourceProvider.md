---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: de2a213122f756d87255be6195759e467f64b428
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772530"
---
# <span data-ttu-id="fe904-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="fe904-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="fe904-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe904-102">SYNOPSIS</span></span>
<span data-ttu-id="fe904-103">Cancela o registro de um provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe904-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="fe904-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe904-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe904-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe904-105">DESCRIPTION</span></span>
<span data-ttu-id="fe904-106">O cmdlet **Unregister-AzResourceProvider** cancela o registro de um provedor de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="fe904-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="fe904-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe904-107">EXAMPLES</span></span>

## <span data-ttu-id="fe904-108">OS</span><span class="sxs-lookup"><span data-stu-id="fe904-108">PARAMETERS</span></span>

### <span data-ttu-id="fe904-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fe904-109">-ApiVersion</span></span>
<span data-ttu-id="fe904-110">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe904-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="fe904-111">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="fe904-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="fe904-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe904-112">-DefaultProfile</span></span>
<span data-ttu-id="fe904-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fe904-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe904-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="fe904-114">-Pre</span></span>
<span data-ttu-id="fe904-115">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="fe904-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fe904-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="fe904-116">-ProviderNamespace</span></span>
<span data-ttu-id="fe904-117">Especifica o namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe904-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="fe904-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fe904-118">-Confirm</span></span>
<span data-ttu-id="fe904-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe904-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe904-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe904-120">-WhatIf</span></span>
<span data-ttu-id="fe904-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fe904-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe904-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe904-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe904-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe904-123">CommonParameters</span></span>
<span data-ttu-id="fe904-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe904-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe904-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe904-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe904-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe904-126">INPUTS</span></span>

### <span data-ttu-id="fe904-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fe904-127">System.String</span></span>

## <span data-ttu-id="fe904-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe904-128">OUTPUTS</span></span>

### <span data-ttu-id="fe904-129">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="fe904-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="fe904-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe904-130">NOTES</span></span>

## <span data-ttu-id="fe904-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe904-131">RELATED LINKS</span></span>

[<span data-ttu-id="fe904-132">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="fe904-132">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="fe904-133">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="fe904-133">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


