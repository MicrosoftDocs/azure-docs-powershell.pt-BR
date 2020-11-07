---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: c3970b61d53b6afdd214aca5c4ca89c735377713
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771283"
---
# <span data-ttu-id="52d51-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="52d51-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="52d51-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52d51-102">SYNOPSIS</span></span>
<span data-ttu-id="52d51-103">Desabilita o HTTPS do domínio personalizado (preterido).</span><span class="sxs-lookup"><span data-stu-id="52d51-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="52d51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52d51-104">SYNTAX</span></span>

### <span data-ttu-id="52d51-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="52d51-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52d51-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52d51-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52d51-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52d51-107">DESCRIPTION</span></span>
<span data-ttu-id="52d51-108">O cmdlet **Disable-AzCdnCustomDomain** desabilita a entrega https segura de um domínio personalizado CDN.</span><span class="sxs-lookup"><span data-stu-id="52d51-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="52d51-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52d51-109">EXAMPLES</span></span>

### <span data-ttu-id="52d51-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52d51-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="52d51-111">Desabilite a entrega HTTPS do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="52d51-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="52d51-112">OS</span><span class="sxs-lookup"><span data-stu-id="52d51-112">PARAMETERS</span></span>

### <span data-ttu-id="52d51-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="52d51-113">-CustomDomainName</span></span>
<span data-ttu-id="52d51-114">Nome de exibição do domínio personalizado CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="52d51-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="52d51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d51-115">-DefaultProfile</span></span>
<span data-ttu-id="52d51-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52d51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52d51-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="52d51-117">-EndpointName</span></span>
<span data-ttu-id="52d51-118">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="52d51-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="52d51-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52d51-119">-InputObject</span></span>
<span data-ttu-id="52d51-120">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="52d51-120">The custom domain object.</span></span>

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

### <span data-ttu-id="52d51-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52d51-121">-PassThru</span></span>
<span data-ttu-id="52d51-122">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="52d51-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="52d51-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="52d51-123">-ProfileName</span></span>
<span data-ttu-id="52d51-124">Nome do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="52d51-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="52d51-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52d51-125">-ResourceGroupName</span></span>
<span data-ttu-id="52d51-126">O grupo de recursos do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="52d51-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="52d51-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52d51-127">-Confirm</span></span>
<span data-ttu-id="52d51-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52d51-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52d51-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52d51-129">-WhatIf</span></span>
<span data-ttu-id="52d51-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52d51-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52d51-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52d51-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52d51-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d51-132">CommonParameters</span></span>
<span data-ttu-id="52d51-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52d51-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d51-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52d51-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d51-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52d51-135">INPUTS</span></span>

### <span data-ttu-id="52d51-136">Microsoft. Azure. Commands. cdn. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="52d51-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="52d51-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52d51-137">OUTPUTS</span></span>

### <span data-ttu-id="52d51-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52d51-138">System.Boolean</span></span>

## <span data-ttu-id="52d51-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52d51-139">NOTES</span></span>

## <span data-ttu-id="52d51-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52d51-140">RELATED LINKS</span></span>
