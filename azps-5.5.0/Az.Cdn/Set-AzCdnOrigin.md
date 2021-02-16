---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127122"
---
# <span data-ttu-id="6a705-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="6a705-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="6a705-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a705-102">SYNOPSIS</span></span>
<span data-ttu-id="6a705-103">Atualiza um servidor de origem de CDN.</span><span class="sxs-lookup"><span data-stu-id="6a705-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="6a705-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a705-104">SYNTAX</span></span>

### <span data-ttu-id="6a705-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6a705-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a705-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a705-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a705-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a705-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a705-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a705-108">DESCRIPTION</span></span>
<span data-ttu-id="6a705-109">O cmdlet **Set-AzCdnOrigin** atualiza um servidor de origem de REDE de Distribuição de Conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a705-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="6a705-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6a705-110">EXAMPLES</span></span>

## <span data-ttu-id="6a705-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a705-111">PARAMETERS</span></span>

### <span data-ttu-id="6a705-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="6a705-112">-CdnOrigin</span></span>
<span data-ttu-id="6a705-113">Especifica o servidor de origem que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="6a705-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="6a705-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a705-114">-DefaultProfile</span></span>
<span data-ttu-id="6a705-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6a705-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a705-116">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="6a705-116">-EndpointName</span></span>
<span data-ttu-id="6a705-117">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a705-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="6a705-118">-Nomedo Host</span><span class="sxs-lookup"><span data-stu-id="6a705-118">-HostName</span></span>
<span data-ttu-id="6a705-119">Nome do host de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a705-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="6a705-120">-httpPort</span><span class="sxs-lookup"><span data-stu-id="6a705-120">-HttpPort</span></span>
<span data-ttu-id="6a705-121">Porta http de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a705-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="6a705-122">-httpsPort</span><span class="sxs-lookup"><span data-stu-id="6a705-122">-HttpsPort</span></span>
<span data-ttu-id="6a705-123">Porta https de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a705-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="6a705-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="6a705-124">-OriginHostHeader</span></span>
<span data-ttu-id="6a705-125">Azure CDN origin host header.</span><span class="sxs-lookup"><span data-stu-id="6a705-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="6a705-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="6a705-126">-OriginName</span></span>
<span data-ttu-id="6a705-127">Nome de origem do CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a705-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="6a705-128">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="6a705-128">-Priority</span></span>
<span data-ttu-id="6a705-129">Prioridade de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a705-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="6a705-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="6a705-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="6a705-131">Uma mensagem personalizada a ser incluída na solicitação de aprovação para se conectar ao Link Particular.</span><span class="sxs-lookup"><span data-stu-id="6a705-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="6a705-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="6a705-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="6a705-133">Local do link particular de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a705-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="6a705-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="6a705-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="6a705-135">ID do recurso de link privado de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a705-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="6a705-136">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6a705-136">-ProfileName</span></span>
<span data-ttu-id="6a705-137">Nome do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a705-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="6a705-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a705-138">-ResourceGroupName</span></span>
<span data-ttu-id="6a705-139">O grupo de recursos do perfil de CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a705-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="6a705-140">-Peso</span><span class="sxs-lookup"><span data-stu-id="6a705-140">-Weight</span></span>
<span data-ttu-id="6a705-141">Azure CDN origin weight.</span><span class="sxs-lookup"><span data-stu-id="6a705-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="6a705-142">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6a705-142">-Confirm</span></span>
<span data-ttu-id="6a705-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a705-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a705-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a705-144">-WhatIf</span></span>
<span data-ttu-id="6a705-145">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6a705-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a705-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6a705-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a705-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a705-147">CommonParameters</span></span>
<span data-ttu-id="6a705-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a705-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a705-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a705-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a705-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="6a705-150">INPUTS</span></span>

### <span data-ttu-id="6a705-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="6a705-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="6a705-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="6a705-152">OUTPUTS</span></span>

### <span data-ttu-id="6a705-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="6a705-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="6a705-154">Notas</span><span class="sxs-lookup"><span data-stu-id="6a705-154">NOTES</span></span>

## <span data-ttu-id="6a705-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a705-155">RELATED LINKS</span></span>

[<span data-ttu-id="6a705-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="6a705-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


