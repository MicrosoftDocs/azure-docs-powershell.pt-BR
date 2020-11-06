---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 92d94950bc4bc90494482b22b81cbd918c8b6938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432561"
---
# <span data-ttu-id="3d146-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3d146-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="3d146-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d146-102">SYNOPSIS</span></span>
<span data-ttu-id="3d146-103">Registra um provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d146-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d146-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d146-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d146-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d146-105">DESCRIPTION</span></span>
<span data-ttu-id="3d146-106">O cmdlet **Register-AzureRmResourceProvider** registra um provedor de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d146-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="3d146-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d146-107">EXAMPLES</span></span>

## <span data-ttu-id="3d146-108">OS</span><span class="sxs-lookup"><span data-stu-id="3d146-108">PARAMETERS</span></span>

### <span data-ttu-id="3d146-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3d146-109">-ApiVersion</span></span>
<span data-ttu-id="3d146-110">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d146-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="3d146-111">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="3d146-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="3d146-112">-Pre</span><span class="sxs-lookup"><span data-stu-id="3d146-112">-Pre</span></span>
<span data-ttu-id="3d146-113">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="3d146-113">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3d146-114">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="3d146-114">-ProviderNamespace</span></span>
<span data-ttu-id="3d146-115">Especifica o namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d146-115">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="3d146-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d146-116">-Confirm</span></span>
<span data-ttu-id="3d146-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d146-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d146-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d146-118">-WhatIf</span></span>
<span data-ttu-id="3d146-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d146-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d146-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d146-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d146-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d146-121">-DefaultProfile</span></span>
<span data-ttu-id="3d146-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d146-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d146-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d146-123">CommonParameters</span></span>
<span data-ttu-id="3d146-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d146-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d146-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d146-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d146-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d146-126">INPUTS</span></span>

## <span data-ttu-id="3d146-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d146-127">OUTPUTS</span></span>

### <span data-ttu-id="3d146-128">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3d146-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="3d146-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d146-129">NOTES</span></span>

## <span data-ttu-id="3d146-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d146-130">RELATED LINKS</span></span>

[<span data-ttu-id="3d146-131">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3d146-131">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="3d146-132">Cancelar registro-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3d146-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)

