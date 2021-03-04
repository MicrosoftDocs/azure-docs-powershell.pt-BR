---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: 837def99279905e3c647ecd8805ed0284840f5a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888740"
---
# <span data-ttu-id="2d7e1-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="2d7e1-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="2d7e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d7e1-102">SYNOPSIS</span></span>
<span data-ttu-id="2d7e1-103">Desabilita HTTPS de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="2d7e1-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="2d7e1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2d7e1-104">SYNTAX</span></span>

### <span data-ttu-id="2d7e1-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2d7e1-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d7e1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d7e1-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d7e1-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d7e1-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d7e1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2d7e1-108">DESCRIPTION</span></span>
<span data-ttu-id="2d7e1-109">O cmdlet **Disable-AzCdnCustomDomainHttps** desabilita a entrega HTTPS segura de um domínio personalizado cdn.</span><span class="sxs-lookup"><span data-stu-id="2d7e1-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="2d7e1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d7e1-110">EXAMPLES</span></span>

### <span data-ttu-id="2d7e1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2d7e1-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="2d7e1-112">Desabilite a entrega segura do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="2d7e1-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="2d7e1-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2d7e1-113">PARAMETERS</span></span>

### <span data-ttu-id="2d7e1-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="2d7e1-114">-CustomDomainName</span></span>
<span data-ttu-id="2d7e1-115">Nome de exibição de domínio personalizado do Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2d7e1-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="2d7e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d7e1-116">-DefaultProfile</span></span>
<span data-ttu-id="2d7e1-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d7e1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d7e1-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2d7e1-118">-EndpointName</span></span>
<span data-ttu-id="2d7e1-119">Nome do ponto de extremidade cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d7e1-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="2d7e1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d7e1-120">-InputObject</span></span>
<span data-ttu-id="2d7e1-121">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="2d7e1-121">The custom domain object.</span></span>

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

### <span data-ttu-id="2d7e1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d7e1-122">-PassThru</span></span>
<span data-ttu-id="2d7e1-123">Retornar objeto, se especificado.</span><span class="sxs-lookup"><span data-stu-id="2d7e1-123">Return object if specified.</span></span>

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

### <span data-ttu-id="2d7e1-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2d7e1-124">-ProfileName</span></span>
<span data-ttu-id="2d7e1-125">Nome do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d7e1-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="2d7e1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d7e1-126">-ResourceGroupName</span></span>
<span data-ttu-id="2d7e1-127">O grupo de recursos do perfil cdn do Azure</span><span class="sxs-lookup"><span data-stu-id="2d7e1-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="2d7e1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d7e1-128">-ResourceId</span></span>
<span data-ttu-id="2d7e1-129">ResourceId do Domínio Personalizado</span><span class="sxs-lookup"><span data-stu-id="2d7e1-129">ResourceId of the Custom Domain</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d7e1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d7e1-130">-Confirm</span></span>
<span data-ttu-id="2d7e1-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d7e1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d7e1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d7e1-132">-WhatIf</span></span>
<span data-ttu-id="2d7e1-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d7e1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d7e1-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d7e1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d7e1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d7e1-135">CommonParameters</span></span>
<span data-ttu-id="2d7e1-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d7e1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d7e1-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d7e1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d7e1-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d7e1-138">INPUTS</span></span>

### <span data-ttu-id="2d7e1-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2d7e1-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="2d7e1-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2d7e1-140">System.String</span></span>

## <span data-ttu-id="2d7e1-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2d7e1-141">OUTPUTS</span></span>

### <span data-ttu-id="2d7e1-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2d7e1-142">System.Boolean</span></span>

## <span data-ttu-id="2d7e1-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="2d7e1-143">NOTES</span></span>

## <span data-ttu-id="2d7e1-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d7e1-144">RELATED LINKS</span></span>
