---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
ms.openlocfilehash: ec15b97aa87c5e581069606a425f25b71dd495dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603403"
---
# <span data-ttu-id="ea783-101">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ea783-101">New-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="ea783-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea783-102">SYNOPSIS</span></span>
<span data-ttu-id="ea783-103">Cria um domínio personalizado para um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="ea783-103">Creates a custom domain for a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea783-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea783-104">SYNTAX</span></span>

### <span data-ttu-id="ea783-105">Conjunto de parâmetros para parâmetros de campos (padrão)</span><span class="sxs-lookup"><span data-stu-id="ea783-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea783-106">Conjunto de parâmetros para parâmetros de objeto</span><span class="sxs-lookup"><span data-stu-id="ea783-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea783-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea783-107">DESCRIPTION</span></span>
<span data-ttu-id="ea783-108">O cmdlet **New-AzureRmCdnCustomDomain** cria um domínio personalizado para o ponto de extremidade da rede de distribuição de conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea783-108">The **New-AzureRmCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="ea783-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea783-109">EXAMPLES</span></span>

## <span data-ttu-id="ea783-110">OS</span><span class="sxs-lookup"><span data-stu-id="ea783-110">PARAMETERS</span></span>

### <span data-ttu-id="ea783-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ea783-111">-CdnEndpoint</span></span>
<span data-ttu-id="ea783-112">Especifica o objeto de ponto de extremidade CDN ao qual o domínio personalizado é adicionado.</span><span class="sxs-lookup"><span data-stu-id="ea783-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea783-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="ea783-113">-CustomDomainName</span></span>
<span data-ttu-id="ea783-114">Especifica o nome do recurso do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="ea783-114">Specifies the resource name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea783-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ea783-115">-EndpointName</span></span>
<span data-ttu-id="ea783-116">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="ea783-116">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea783-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="ea783-117">-HostName</span></span>
<span data-ttu-id="ea783-118">Especifica o nome do host do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="ea783-118">Specifies the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea783-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ea783-119">-ProfileName</span></span>
<span data-ttu-id="ea783-120">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="ea783-120">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea783-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea783-121">-ResourceGroupName</span></span>
<span data-ttu-id="ea783-122">Especifica o nome do grupo de recursos ao qual pertence o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="ea783-122">Specifies the name of the resource group to which the custom domain belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea783-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ea783-123">-Confirm</span></span>
<span data-ttu-id="ea783-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea783-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea783-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea783-125">-WhatIf</span></span>
<span data-ttu-id="ea783-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ea783-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea783-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea783-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea783-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea783-128">-DefaultProfile</span></span>
<span data-ttu-id="ea783-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea783-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea783-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea783-130">CommonParameters</span></span>
<span data-ttu-id="ea783-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea783-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea783-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea783-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea783-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea783-133">INPUTS</span></span>

### <span data-ttu-id="ea783-134">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ea783-134">PSEndpoint</span></span>
<span data-ttu-id="ea783-135">O parâmetro ' CdnEndpoint ' aceita o valor do tipo ' PSEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ea783-135">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="ea783-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea783-136">OUTPUTS</span></span>

### <span data-ttu-id="ea783-137">Microsoft. Azure. Commands. cdn. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ea783-137">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="ea783-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea783-138">NOTES</span></span>

## <span data-ttu-id="ea783-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea783-139">RELATED LINKS</span></span>

[<span data-ttu-id="ea783-140">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ea783-140">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="ea783-141">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ea783-141">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="ea783-142">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ea783-142">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


