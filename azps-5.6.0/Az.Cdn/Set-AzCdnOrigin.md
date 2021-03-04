---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 5636aeef0b1c04ffbb0faa7e44161628824e9f1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893399"
---
# <span data-ttu-id="fc334-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="fc334-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="fc334-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc334-102">SYNOPSIS</span></span>
<span data-ttu-id="fc334-103">Atualiza um servidor de origem da CDN.</span><span class="sxs-lookup"><span data-stu-id="fc334-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="fc334-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fc334-104">SYNTAX</span></span>

### <span data-ttu-id="fc334-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fc334-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc334-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc334-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc334-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc334-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc334-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fc334-108">DESCRIPTION</span></span>
<span data-ttu-id="fc334-109">O cmdlet **Set-AzCdnOrigin** atualiza um servidor de origem da Rede de Distribuição de Conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc334-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="fc334-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc334-110">EXAMPLES</span></span>

## <span data-ttu-id="fc334-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fc334-111">PARAMETERS</span></span>

### <span data-ttu-id="fc334-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="fc334-112">-CdnOrigin</span></span>
<span data-ttu-id="fc334-113">Especifica o servidor de origem que esse cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="fc334-113">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc334-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc334-114">-DefaultProfile</span></span>
<span data-ttu-id="fc334-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fc334-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc334-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fc334-116">-EndpointName</span></span>
<span data-ttu-id="fc334-117">Nome do ponto de extremidade cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc334-117">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc334-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="fc334-118">-HostName</span></span>
<span data-ttu-id="fc334-119">Nome do host de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc334-119">Azure CDN origin host name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc334-120">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="fc334-120">-HttpPort</span></span>
<span data-ttu-id="fc334-121">Porta http de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc334-121">Azure CDN origin http port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc334-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="fc334-122">-HttpsPort</span></span>
<span data-ttu-id="fc334-123">Porta https de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc334-123">Azure CDN origin https port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc334-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="fc334-124">-OriginHostHeader</span></span>
<span data-ttu-id="fc334-125">Header de host de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc334-125">Azure CDN origin host header.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc334-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="fc334-126">-OriginName</span></span>
<span data-ttu-id="fc334-127">Nome de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc334-127">Azure CDN origin name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc334-128">-Priority</span><span class="sxs-lookup"><span data-stu-id="fc334-128">-Priority</span></span>
<span data-ttu-id="fc334-129">Prioridade de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc334-129">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc334-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="fc334-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="fc334-131">Uma mensagem personalizada a ser incluída na solicitação de aprovação para se conectar ao Link Particular.</span><span class="sxs-lookup"><span data-stu-id="fc334-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc334-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="fc334-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="fc334-133">Local do link privado de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc334-133">Azure CDN origin private link location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc334-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="fc334-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="fc334-135">ID do recurso de link privado de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc334-135">Azure CDN origin private link resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc334-136">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fc334-136">-ProfileName</span></span>
<span data-ttu-id="fc334-137">Nome do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc334-137">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc334-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc334-138">-ResourceGroupName</span></span>
<span data-ttu-id="fc334-139">O grupo de recursos do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc334-139">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc334-140">-Weight</span><span class="sxs-lookup"><span data-stu-id="fc334-140">-Weight</span></span>
<span data-ttu-id="fc334-141">Peso de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc334-141">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc334-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc334-142">-Confirm</span></span>
<span data-ttu-id="fc334-143">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc334-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc334-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc334-144">-WhatIf</span></span>
<span data-ttu-id="fc334-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc334-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc334-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc334-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc334-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc334-147">CommonParameters</span></span>
<span data-ttu-id="fc334-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc334-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc334-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc334-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc334-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc334-150">INPUTS</span></span>

### <span data-ttu-id="fc334-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="fc334-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="fc334-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fc334-152">OUTPUTS</span></span>

### <span data-ttu-id="fc334-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="fc334-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="fc334-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="fc334-154">NOTES</span></span>

## <span data-ttu-id="fc334-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc334-155">RELATED LINKS</span></span>

[<span data-ttu-id="fc334-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="fc334-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


