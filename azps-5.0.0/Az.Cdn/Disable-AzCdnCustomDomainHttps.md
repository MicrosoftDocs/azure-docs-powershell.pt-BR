---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: be3e4d0437e24a282c1933cf82e1818dd9f88221
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125156"
---
# <span data-ttu-id="7a972-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="7a972-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="7a972-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a972-102">SYNOPSIS</span></span>
<span data-ttu-id="7a972-103">Desabilita o HTTPS do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="7a972-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="7a972-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a972-104">SYNTAX</span></span>

### <span data-ttu-id="7a972-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7a972-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a972-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a972-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a972-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a972-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a972-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a972-108">DESCRIPTION</span></span>
<span data-ttu-id="7a972-109">O cmdlet **Disable-AzCdnCustomDomainHttps** desabilita a entrega https segura de um domínio personalizado CDN.</span><span class="sxs-lookup"><span data-stu-id="7a972-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="7a972-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a972-110">EXAMPLES</span></span>

### <span data-ttu-id="7a972-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a972-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="7a972-112">Desabilitar a entrega segura do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="7a972-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="7a972-113">OS</span><span class="sxs-lookup"><span data-stu-id="7a972-113">PARAMETERS</span></span>

### <span data-ttu-id="7a972-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="7a972-114">-CustomDomainName</span></span>
<span data-ttu-id="7a972-115">Nome de exibição do domínio personalizado CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a972-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="7a972-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a972-116">-DefaultProfile</span></span>
<span data-ttu-id="7a972-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a972-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a972-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7a972-118">-EndpointName</span></span>
<span data-ttu-id="7a972-119">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a972-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="7a972-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a972-120">-InputObject</span></span>
<span data-ttu-id="7a972-121">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="7a972-121">The custom domain object.</span></span>

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

### <span data-ttu-id="7a972-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a972-122">-PassThru</span></span>
<span data-ttu-id="7a972-123">Objeto de retorno, se especificado.</span><span class="sxs-lookup"><span data-stu-id="7a972-123">Return object if specified.</span></span>

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

### <span data-ttu-id="7a972-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7a972-124">-ProfileName</span></span>
<span data-ttu-id="7a972-125">Nome do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a972-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="7a972-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a972-126">-ResourceGroupName</span></span>
<span data-ttu-id="7a972-127">O grupo de recursos do perfil CDN do Azure</span><span class="sxs-lookup"><span data-stu-id="7a972-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="7a972-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a972-128">-ResourceId</span></span>
<span data-ttu-id="7a972-129">ResourceId do domínio personalizado</span><span class="sxs-lookup"><span data-stu-id="7a972-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="7a972-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7a972-130">-Confirm</span></span>
<span data-ttu-id="7a972-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a972-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a972-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a972-132">-WhatIf</span></span>
<span data-ttu-id="7a972-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7a972-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a972-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a972-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a972-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a972-135">CommonParameters</span></span>
<span data-ttu-id="7a972-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a972-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a972-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a972-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a972-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a972-138">INPUTS</span></span>

### <span data-ttu-id="7a972-139">Microsoft. Azure. Commands. cdn. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7a972-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="7a972-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7a972-140">System.String</span></span>

## <span data-ttu-id="7a972-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a972-141">OUTPUTS</span></span>

### <span data-ttu-id="7a972-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7a972-142">System.Boolean</span></span>

## <span data-ttu-id="7a972-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a972-143">NOTES</span></span>

## <span data-ttu-id="7a972-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a972-144">RELATED LINKS</span></span>
