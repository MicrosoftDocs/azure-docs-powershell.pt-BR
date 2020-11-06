---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/enable-azurermcdncustomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Enable-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Enable-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 50c1bf02a8952bbbddd2bbb82e55441adacd6a2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426428"
---
# <span data-ttu-id="33d97-101">Enable-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="33d97-101">Enable-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="33d97-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33d97-102">SYNOPSIS</span></span>
<span data-ttu-id="33d97-103">Habilita HTTPS personalizado.</span><span class="sxs-lookup"><span data-stu-id="33d97-103">Enables custom HTTPS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33d97-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33d97-104">SYNTAX</span></span>

### <span data-ttu-id="33d97-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="33d97-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33d97-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33d97-106">ByObjectParameterSet</span></span>
```
Enable-AzureRmCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33d97-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33d97-107">DESCRIPTION</span></span>
<span data-ttu-id="33d97-108">O cmdlet **Enable-AzureRmCdnCustomDomain** habilita a entrega https segura de um domínio personalizado CDN.</span><span class="sxs-lookup"><span data-stu-id="33d97-108">The **Enable-AzureRmCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="33d97-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33d97-109">EXAMPLES</span></span>

### <span data-ttu-id="33d97-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="33d97-110">Example 1</span></span>
```powershell
Enable-AzureRmCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="33d97-111">Habilite a entrega HTTPS do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="33d97-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="33d97-112">OS</span><span class="sxs-lookup"><span data-stu-id="33d97-112">PARAMETERS</span></span>

### <span data-ttu-id="33d97-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="33d97-113">-CustomDomainName</span></span>
<span data-ttu-id="33d97-114">Nome de exibição do domínio personalizado CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="33d97-114">Azure CDN custom domain display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33d97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d97-115">-DefaultProfile</span></span>
<span data-ttu-id="33d97-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33d97-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33d97-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="33d97-117">-EndpointName</span></span>
<span data-ttu-id="33d97-118">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="33d97-118">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33d97-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33d97-119">-InputObject</span></span>
<span data-ttu-id="33d97-120">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="33d97-120">The custom domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33d97-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33d97-121">-PassThru</span></span>
<span data-ttu-id="33d97-122">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="33d97-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="33d97-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="33d97-123">-ProfileName</span></span>
<span data-ttu-id="33d97-124">Nome do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="33d97-124">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33d97-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33d97-125">-ResourceGroupName</span></span>
<span data-ttu-id="33d97-126">O grupo de recursos do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="33d97-126">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33d97-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="33d97-127">-Confirm</span></span>
<span data-ttu-id="33d97-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33d97-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33d97-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33d97-129">-WhatIf</span></span>
<span data-ttu-id="33d97-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="33d97-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33d97-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33d97-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33d97-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d97-132">CommonParameters</span></span>
<span data-ttu-id="33d97-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33d97-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d97-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33d97-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d97-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33d97-135">INPUTS</span></span>

### <span data-ttu-id="33d97-136">Microsoft. Azure. Commands. cdn. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="33d97-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="33d97-137">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="33d97-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="33d97-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33d97-138">OUTPUTS</span></span>

### <span data-ttu-id="33d97-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="33d97-139">System.Boolean</span></span>

## <span data-ttu-id="33d97-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33d97-140">NOTES</span></span>

## <span data-ttu-id="33d97-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33d97-141">RELATED LINKS</span></span>
