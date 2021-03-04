---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: cc7350fb76091d3bf2f8bdab5c037a5afbe8b57a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889313"
---
# <span data-ttu-id="270c1-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="270c1-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="270c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="270c1-102">SYNOPSIS</span></span>
<span data-ttu-id="270c1-103">Cria uma nova origem de CDN</span><span class="sxs-lookup"><span data-stu-id="270c1-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="270c1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="270c1-104">SYNTAX</span></span>

### <span data-ttu-id="270c1-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="270c1-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="270c1-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="270c1-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="270c1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="270c1-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="270c1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="270c1-108">DESCRIPTION</span></span>
<span data-ttu-id="270c1-109">O New-AzCdnOrigin criará uma nova origem de CDN no ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="270c1-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="270c1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="270c1-110">EXAMPLES</span></span>

### <span data-ttu-id="270c1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="270c1-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="270c1-112">Este cmdlet criará uma nova origem de CDN para o ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="270c1-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="270c1-113">Ele usará o nome do host fornecido como a origem.</span><span class="sxs-lookup"><span data-stu-id="270c1-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="270c1-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="270c1-114">PARAMETERS</span></span>

### <span data-ttu-id="270c1-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="270c1-115">-CdnOrigin</span></span>
<span data-ttu-id="270c1-116">O objeto de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="270c1-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="270c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="270c1-117">-DefaultProfile</span></span>
<span data-ttu-id="270c1-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="270c1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="270c1-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="270c1-119">-EndpointName</span></span>
<span data-ttu-id="270c1-120">Nome do ponto de extremidade cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="270c1-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="270c1-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="270c1-121">-HostName</span></span>
<span data-ttu-id="270c1-122">Nome do host de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="270c1-122">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="270c1-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="270c1-123">-HttpPort</span></span>
<span data-ttu-id="270c1-124">Porta http de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="270c1-124">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="270c1-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="270c1-125">-HttpsPort</span></span>
<span data-ttu-id="270c1-126">Porta https de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="270c1-126">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="270c1-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="270c1-127">-OriginHostHeader</span></span>
<span data-ttu-id="270c1-128">Header de host de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="270c1-128">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="270c1-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="270c1-129">-OriginName</span></span>
<span data-ttu-id="270c1-130">Nome de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="270c1-130">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="270c1-131">-Priority</span><span class="sxs-lookup"><span data-stu-id="270c1-131">-Priority</span></span>
<span data-ttu-id="270c1-132">Prioridade de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="270c1-132">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="270c1-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="270c1-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="270c1-134">Uma mensagem personalizada a ser incluída na solicitação de aprovação para se conectar ao Link Particular.</span><span class="sxs-lookup"><span data-stu-id="270c1-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="270c1-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="270c1-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="270c1-136">Local do link privado de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="270c1-136">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="270c1-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="270c1-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="270c1-138">ID do recurso de link privado de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="270c1-138">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="270c1-139">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="270c1-139">-ProfileName</span></span>
<span data-ttu-id="270c1-140">Nome do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="270c1-140">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="270c1-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="270c1-141">-ResourceGroupName</span></span>
<span data-ttu-id="270c1-142">O grupo de recursos do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="270c1-142">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="270c1-143">-Weight</span><span class="sxs-lookup"><span data-stu-id="270c1-143">-Weight</span></span>
<span data-ttu-id="270c1-144">Peso de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="270c1-144">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="270c1-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="270c1-145">-Confirm</span></span>
<span data-ttu-id="270c1-146">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="270c1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="270c1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="270c1-147">-WhatIf</span></span>
<span data-ttu-id="270c1-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="270c1-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="270c1-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="270c1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="270c1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270c1-150">CommonParameters</span></span>
<span data-ttu-id="270c1-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="270c1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270c1-152">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="270c1-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270c1-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="270c1-153">INPUTS</span></span>

### <span data-ttu-id="270c1-154">Nenhum</span><span class="sxs-lookup"><span data-stu-id="270c1-154">None</span></span>

## <span data-ttu-id="270c1-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="270c1-155">OUTPUTS</span></span>

### <span data-ttu-id="270c1-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="270c1-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="270c1-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="270c1-157">NOTES</span></span>

## <span data-ttu-id="270c1-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="270c1-158">RELATED LINKS</span></span>
