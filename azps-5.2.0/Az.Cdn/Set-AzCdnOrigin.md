---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263499"
---
# <span data-ttu-id="af84e-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="af84e-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="af84e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af84e-102">SYNOPSIS</span></span>
<span data-ttu-id="af84e-103">Atualiza um servidor de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="af84e-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="af84e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af84e-104">SYNTAX</span></span>

### <span data-ttu-id="af84e-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="af84e-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af84e-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="af84e-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af84e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af84e-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af84e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af84e-108">DESCRIPTION</span></span>
<span data-ttu-id="af84e-109">O cmdlet **set-AzCdnOrigin** atualiza um servidor de origem da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="af84e-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="af84e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af84e-110">EXAMPLES</span></span>

## <span data-ttu-id="af84e-111">OS</span><span class="sxs-lookup"><span data-stu-id="af84e-111">PARAMETERS</span></span>

### <span data-ttu-id="af84e-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="af84e-112">-CdnOrigin</span></span>
<span data-ttu-id="af84e-113">Especifica o servidor de origem no qual esse cmdlet é atualizado.</span><span class="sxs-lookup"><span data-stu-id="af84e-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="af84e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af84e-114">-DefaultProfile</span></span>
<span data-ttu-id="af84e-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="af84e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af84e-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="af84e-116">-EndpointName</span></span>
<span data-ttu-id="af84e-117">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="af84e-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="af84e-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="af84e-118">-HostName</span></span>
<span data-ttu-id="af84e-119">Nome do host da origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="af84e-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="af84e-120">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="af84e-120">-HttpPort</span></span>
<span data-ttu-id="af84e-121">Porta http da origem CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="af84e-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="af84e-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="af84e-122">-HttpsPort</span></span>
<span data-ttu-id="af84e-123">Porta https da origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="af84e-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="af84e-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="af84e-124">-OriginHostHeader</span></span>
<span data-ttu-id="af84e-125">Cabeçalho do host de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="af84e-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="af84e-126">-Originname</span><span class="sxs-lookup"><span data-stu-id="af84e-126">-OriginName</span></span>
<span data-ttu-id="af84e-127">Nome da origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="af84e-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="af84e-128">-Priority</span><span class="sxs-lookup"><span data-stu-id="af84e-128">-Priority</span></span>
<span data-ttu-id="af84e-129">Prioridade de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="af84e-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="af84e-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="af84e-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="af84e-131">Uma mensagem personalizada a ser incluída na solicitação de aprovação para se conectar ao link particular.</span><span class="sxs-lookup"><span data-stu-id="af84e-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="af84e-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="af84e-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="af84e-133">Local do link particular de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="af84e-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="af84e-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="af84e-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="af84e-135">ID do recurso do link privado da origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="af84e-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="af84e-136">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="af84e-136">-ProfileName</span></span>
<span data-ttu-id="af84e-137">Nome do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="af84e-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="af84e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af84e-138">-ResourceGroupName</span></span>
<span data-ttu-id="af84e-139">O grupo de recursos do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="af84e-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="af84e-140">-Weight</span><span class="sxs-lookup"><span data-stu-id="af84e-140">-Weight</span></span>
<span data-ttu-id="af84e-141">Peso da origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="af84e-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="af84e-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af84e-142">-Confirm</span></span>
<span data-ttu-id="af84e-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af84e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af84e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af84e-144">-WhatIf</span></span>
<span data-ttu-id="af84e-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af84e-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af84e-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af84e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af84e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af84e-147">CommonParameters</span></span>
<span data-ttu-id="af84e-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af84e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af84e-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af84e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af84e-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af84e-150">INPUTS</span></span>

### <span data-ttu-id="af84e-151">Microsoft. Azure. Commands. cdn. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="af84e-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="af84e-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af84e-152">OUTPUTS</span></span>

### <span data-ttu-id="af84e-153">Microsoft. Azure. Commands. cdn. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="af84e-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="af84e-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af84e-154">NOTES</span></span>

## <span data-ttu-id="af84e-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af84e-155">RELATED LINKS</span></span>

[<span data-ttu-id="af84e-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="af84e-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


