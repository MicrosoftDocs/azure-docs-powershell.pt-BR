---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
ms.openlocfilehash: 2371ea9a50af1d23144560acbf4fd88679f0e50d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786226"
---
# <span data-ttu-id="861a5-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="861a5-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="861a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="861a5-102">SYNOPSIS</span></span>
<span data-ttu-id="861a5-103">Registra um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="861a5-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="861a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="861a5-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="861a5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="861a5-105">DESCRIPTION</span></span>
<span data-ttu-id="861a5-106">O cmdlet **Register-AzureRmProviderFeature** registra um recurso de provedor do Azure em sua conta.</span><span class="sxs-lookup"><span data-stu-id="861a5-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="861a5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="861a5-107">EXAMPLES</span></span>

### <span data-ttu-id="861a5-108">Exemplo 1: registrar um recurso</span><span class="sxs-lookup"><span data-stu-id="861a5-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="861a5-109">Isso adiciona o recurso AllowApplicationSecurityGroups para a Microsoft. Network à sua conta.</span><span class="sxs-lookup"><span data-stu-id="861a5-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="861a5-110">OS</span><span class="sxs-lookup"><span data-stu-id="861a5-110">PARAMETERS</span></span>

### <span data-ttu-id="861a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="861a5-111">-DefaultProfile</span></span>
<span data-ttu-id="861a5-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="861a5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="861a5-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="861a5-113">-FeatureName</span></span>
<span data-ttu-id="861a5-114">Especifica o nome do recurso registrado por este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="861a5-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="861a5-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="861a5-115">-ProviderNamespace</span></span>
<span data-ttu-id="861a5-116">Especifica um namespace para o qual esse cmdlet registra um recurso de provedor.</span><span class="sxs-lookup"><span data-stu-id="861a5-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="861a5-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="861a5-117">-Confirm</span></span>
<span data-ttu-id="861a5-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="861a5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="861a5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="861a5-119">-WhatIf</span></span>
<span data-ttu-id="861a5-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="861a5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="861a5-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="861a5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="861a5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="861a5-122">CommonParameters</span></span>
<span data-ttu-id="861a5-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="861a5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="861a5-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="861a5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="861a5-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="861a5-125">INPUTS</span></span>

## <span data-ttu-id="861a5-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="861a5-126">OUTPUTS</span></span>

## <span data-ttu-id="861a5-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="861a5-127">NOTES</span></span>

## <span data-ttu-id="861a5-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="861a5-128">RELATED LINKS</span></span>

[<span data-ttu-id="861a5-129">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="861a5-129">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


