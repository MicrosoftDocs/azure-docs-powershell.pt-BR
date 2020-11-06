---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b41f7cb1c5e3ebec58e3866c94d8e2c62bdf670b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428783"
---
# <span data-ttu-id="7f17b-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7f17b-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="7f17b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f17b-102">SYNOPSIS</span></span>
<span data-ttu-id="7f17b-103">Registra um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="7f17b-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f17b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f17b-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f17b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f17b-105">DESCRIPTION</span></span>
<span data-ttu-id="7f17b-106">O cmdlet **Register-AzureRmProviderFeature** registra um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="7f17b-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="7f17b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f17b-107">EXAMPLES</span></span>

### <span data-ttu-id="7f17b-108">Exemplo 1: registrar um recurso</span><span class="sxs-lookup"><span data-stu-id="7f17b-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="7f17b-109">Isso adiciona o recurso AllowApplicationSecurityGroups para a Microsoft. Network à sua conta.</span><span class="sxs-lookup"><span data-stu-id="7f17b-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="7f17b-110">OS</span><span class="sxs-lookup"><span data-stu-id="7f17b-110">PARAMETERS</span></span>

### <span data-ttu-id="7f17b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f17b-111">-DefaultProfile</span></span>
<span data-ttu-id="7f17b-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7f17b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f17b-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="7f17b-113">-FeatureName</span></span>
<span data-ttu-id="7f17b-114">Especifica o nome do recurso registrado por este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f17b-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="7f17b-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="7f17b-115">-ProviderNamespace</span></span>
<span data-ttu-id="7f17b-116">Especifica um namespace para o qual esse cmdlet registra um recurso de provedor.</span><span class="sxs-lookup"><span data-stu-id="7f17b-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="7f17b-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7f17b-117">-Confirm</span></span>
<span data-ttu-id="7f17b-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f17b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f17b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f17b-119">-WhatIf</span></span>
<span data-ttu-id="7f17b-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7f17b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f17b-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7f17b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f17b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f17b-122">CommonParameters</span></span>
<span data-ttu-id="7f17b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f17b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f17b-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f17b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f17b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f17b-125">INPUTS</span></span>

### <span data-ttu-id="7f17b-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7f17b-126">None</span></span>
<span data-ttu-id="7f17b-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="7f17b-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7f17b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f17b-128">OUTPUTS</span></span>

### <span data-ttu-id="7f17b-129">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="7f17b-129">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="7f17b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f17b-130">NOTES</span></span>

## <span data-ttu-id="7f17b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f17b-131">RELATED LINKS</span></span>

[<span data-ttu-id="7f17b-132">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7f17b-132">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


