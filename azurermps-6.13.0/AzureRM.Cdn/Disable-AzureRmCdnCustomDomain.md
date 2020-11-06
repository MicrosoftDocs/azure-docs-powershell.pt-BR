---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/disable-azurermcdncustomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Disable-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Disable-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 1f0694d93f95f9fed6f23d7912003a179598ac91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431394"
---
# <span data-ttu-id="01a44-101">Disable-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="01a44-101">Disable-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="01a44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01a44-102">SYNOPSIS</span></span>
<span data-ttu-id="01a44-103">Desabilita a HTTPS personalizada.</span><span class="sxs-lookup"><span data-stu-id="01a44-103">Disables custom HTTPS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01a44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01a44-104">SYNTAX</span></span>

### <span data-ttu-id="01a44-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="01a44-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01a44-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01a44-106">ByObjectParameterSet</span></span>
```
Disable-AzureRmCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01a44-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01a44-107">DESCRIPTION</span></span>
<span data-ttu-id="01a44-108">O cmdlet **Disable-AzureRmCdnCustomDomain** desabilita a entrega https segura de um domínio personalizado CDN.</span><span class="sxs-lookup"><span data-stu-id="01a44-108">The **Disable-AzureRmCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="01a44-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01a44-109">EXAMPLES</span></span>

### <span data-ttu-id="01a44-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="01a44-110">Example 1</span></span>
```powershell
Disable-AzureRmCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="01a44-111">Desabilite a entrega HTTPS do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="01a44-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="01a44-112">OS</span><span class="sxs-lookup"><span data-stu-id="01a44-112">PARAMETERS</span></span>

### <span data-ttu-id="01a44-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="01a44-113">-CustomDomainName</span></span>
<span data-ttu-id="01a44-114">Nome de exibição do domínio personalizado CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="01a44-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="01a44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a44-115">-DefaultProfile</span></span>
<span data-ttu-id="01a44-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01a44-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01a44-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="01a44-117">-EndpointName</span></span>
<span data-ttu-id="01a44-118">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="01a44-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="01a44-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01a44-119">-InputObject</span></span>
<span data-ttu-id="01a44-120">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="01a44-120">The custom domain object.</span></span>

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

### <span data-ttu-id="01a44-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01a44-121">-PassThru</span></span>
<span data-ttu-id="01a44-122">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="01a44-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="01a44-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="01a44-123">-ProfileName</span></span>
<span data-ttu-id="01a44-124">Nome do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="01a44-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="01a44-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01a44-125">-ResourceGroupName</span></span>
<span data-ttu-id="01a44-126">O grupo de recursos do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="01a44-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="01a44-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="01a44-127">-Confirm</span></span>
<span data-ttu-id="01a44-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01a44-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01a44-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01a44-129">-WhatIf</span></span>
<span data-ttu-id="01a44-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="01a44-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01a44-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="01a44-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01a44-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a44-132">CommonParameters</span></span>
<span data-ttu-id="01a44-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01a44-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a44-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01a44-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a44-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="01a44-135">INPUTS</span></span>

### <span data-ttu-id="01a44-136">Microsoft. Azure. Commands. cdn. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="01a44-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="01a44-137">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="01a44-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="01a44-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01a44-138">OUTPUTS</span></span>

### <span data-ttu-id="01a44-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01a44-139">System.Boolean</span></span>

## <span data-ttu-id="01a44-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01a44-140">NOTES</span></span>

## <span data-ttu-id="01a44-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01a44-141">RELATED LINKS</span></span>
