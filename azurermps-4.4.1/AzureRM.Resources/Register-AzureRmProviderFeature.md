---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b519108918f2c26d86807302314a4defed1a0050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432566"
---
# <span data-ttu-id="378c2-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="378c2-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="378c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="378c2-102">SYNOPSIS</span></span>
<span data-ttu-id="378c2-103">Registra um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="378c2-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="378c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="378c2-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="378c2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="378c2-105">DESCRIPTION</span></span>
<span data-ttu-id="378c2-106">O cmdlet **Register-AzureRmProviderFeature** registra um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="378c2-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="378c2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="378c2-107">EXAMPLES</span></span>

## <span data-ttu-id="378c2-108">OS</span><span class="sxs-lookup"><span data-stu-id="378c2-108">PARAMETERS</span></span>

### <span data-ttu-id="378c2-109">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="378c2-109">-FeatureName</span></span>
<span data-ttu-id="378c2-110">Especifica o nome do recurso registrado por este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="378c2-110">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="378c2-111">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="378c2-111">-ProviderNamespace</span></span>
<span data-ttu-id="378c2-112">Especifica um namespace para o qual esse cmdlet registra um recurso de provedor.</span><span class="sxs-lookup"><span data-stu-id="378c2-112">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="378c2-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="378c2-113">-Confirm</span></span>
<span data-ttu-id="378c2-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="378c2-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="378c2-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="378c2-115">-WhatIf</span></span>
<span data-ttu-id="378c2-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="378c2-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="378c2-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="378c2-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="378c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="378c2-118">-DefaultProfile</span></span>
<span data-ttu-id="378c2-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="378c2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="378c2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="378c2-120">CommonParameters</span></span>
<span data-ttu-id="378c2-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="378c2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="378c2-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="378c2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="378c2-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="378c2-123">INPUTS</span></span>

## <span data-ttu-id="378c2-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="378c2-124">OUTPUTS</span></span>

### <span data-ttu-id="378c2-125">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="378c2-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="378c2-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="378c2-126">NOTES</span></span>

## <span data-ttu-id="378c2-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="378c2-127">RELATED LINKS</span></span>

[<span data-ttu-id="378c2-128">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="378c2-128">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


