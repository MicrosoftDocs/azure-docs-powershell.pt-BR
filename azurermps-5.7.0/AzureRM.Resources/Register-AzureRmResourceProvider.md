---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 9e379df74f974e303faac300515e6bb7844e770b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603226"
---
# <span data-ttu-id="62ee6-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="62ee6-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="62ee6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62ee6-102">SYNOPSIS</span></span>
<span data-ttu-id="62ee6-103">Registra um provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="62ee6-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62ee6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62ee6-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62ee6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62ee6-105">DESCRIPTION</span></span>
<span data-ttu-id="62ee6-106">O cmdlet **Register-AzureRmResourceProvider** registra um provedor de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="62ee6-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="62ee6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62ee6-107">EXAMPLES</span></span>

### <span data-ttu-id="62ee6-108">Exemplo 1: registrar um provedor</span><span class="sxs-lookup"><span data-stu-id="62ee6-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzureRmResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="62ee6-109">Isso registra o provedor Microsoft. Network para a sua conta.</span><span class="sxs-lookup"><span data-stu-id="62ee6-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="62ee6-110">OS</span><span class="sxs-lookup"><span data-stu-id="62ee6-110">PARAMETERS</span></span>

### <span data-ttu-id="62ee6-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="62ee6-111">-ApiVersion</span></span>
<span data-ttu-id="62ee6-112">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="62ee6-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="62ee6-113">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="62ee6-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="62ee6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ee6-114">-DefaultProfile</span></span>
<span data-ttu-id="62ee6-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="62ee6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62ee6-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="62ee6-116">-Pre</span></span>
<span data-ttu-id="62ee6-117">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="62ee6-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="62ee6-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="62ee6-118">-ProviderNamespace</span></span>
<span data-ttu-id="62ee6-119">Especifica o namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="62ee6-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="62ee6-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="62ee6-120">-Confirm</span></span>
<span data-ttu-id="62ee6-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62ee6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62ee6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62ee6-122">-WhatIf</span></span>
<span data-ttu-id="62ee6-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="62ee6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62ee6-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="62ee6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62ee6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ee6-125">CommonParameters</span></span>
<span data-ttu-id="62ee6-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62ee6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ee6-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62ee6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ee6-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62ee6-128">INPUTS</span></span>

### <span data-ttu-id="62ee6-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="62ee6-129">None</span></span>
<span data-ttu-id="62ee6-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="62ee6-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62ee6-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62ee6-131">OUTPUTS</span></span>

### <span data-ttu-id="62ee6-132">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="62ee6-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="62ee6-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62ee6-133">NOTES</span></span>

## <span data-ttu-id="62ee6-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62ee6-134">RELATED LINKS</span></span>

[<span data-ttu-id="62ee6-135">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="62ee6-135">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="62ee6-136">Cancelar registro-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="62ee6-136">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


