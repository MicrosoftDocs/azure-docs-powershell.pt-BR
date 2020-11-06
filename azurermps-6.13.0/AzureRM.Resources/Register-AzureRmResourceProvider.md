---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 691378cac3ac721084315a1708bf8d4d0a24dc92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428373"
---
# <span data-ttu-id="3d74a-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3d74a-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="3d74a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d74a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d74a-103">Registra um provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d74a-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d74a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d74a-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d74a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d74a-105">DESCRIPTION</span></span>
<span data-ttu-id="3d74a-106">O cmdlet **Register-AzureRmResourceProvider** registra um provedor de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d74a-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="3d74a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d74a-107">EXAMPLES</span></span>

### <span data-ttu-id="3d74a-108">Exemplo 1: registrar um provedor</span><span class="sxs-lookup"><span data-stu-id="3d74a-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzureRmResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="3d74a-109">Isso registra o provedor Microsoft. Network para a sua conta.</span><span class="sxs-lookup"><span data-stu-id="3d74a-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="3d74a-110">OS</span><span class="sxs-lookup"><span data-stu-id="3d74a-110">PARAMETERS</span></span>

### <span data-ttu-id="3d74a-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3d74a-111">-ApiVersion</span></span>
<span data-ttu-id="3d74a-112">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d74a-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="3d74a-113">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="3d74a-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="3d74a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d74a-114">-DefaultProfile</span></span>
<span data-ttu-id="3d74a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3d74a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d74a-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="3d74a-116">-Pre</span></span>
<span data-ttu-id="3d74a-117">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="3d74a-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3d74a-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="3d74a-118">-ProviderNamespace</span></span>
<span data-ttu-id="3d74a-119">Especifica o namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d74a-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="3d74a-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d74a-120">-Confirm</span></span>
<span data-ttu-id="3d74a-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d74a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d74a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d74a-122">-WhatIf</span></span>
<span data-ttu-id="3d74a-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d74a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d74a-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d74a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d74a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d74a-125">CommonParameters</span></span>
<span data-ttu-id="3d74a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d74a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d74a-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d74a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d74a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d74a-128">INPUTS</span></span>

## <span data-ttu-id="3d74a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d74a-129">OUTPUTS</span></span>

## <span data-ttu-id="3d74a-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d74a-130">NOTES</span></span>

## <span data-ttu-id="3d74a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d74a-131">RELATED LINKS</span></span>

[<span data-ttu-id="3d74a-132">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3d74a-132">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="3d74a-133">Cancelar registro-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3d74a-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


