---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: a9ef1687333851e2ac67dfb3f0146509f3b77183
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116922"
---
# <span data-ttu-id="08404-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="08404-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="08404-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08404-102">SYNOPSIS</span></span>
<span data-ttu-id="08404-103">Cria uma nova origem de CDN</span><span class="sxs-lookup"><span data-stu-id="08404-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="08404-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08404-104">SYNTAX</span></span>

### <span data-ttu-id="08404-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="08404-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08404-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="08404-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08404-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08404-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08404-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="08404-108">DESCRIPTION</span></span>
<span data-ttu-id="08404-109">A New-AzCdnOrigin criará uma nova origem de CDN dentro do ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="08404-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="08404-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="08404-110">EXAMPLES</span></span>

### <span data-ttu-id="08404-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="08404-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="08404-112">Esse cmdlet criará uma nova origem de CDN para o ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="08404-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="08404-113">Ele usará o nome do host fornecido como a origem.</span><span class="sxs-lookup"><span data-stu-id="08404-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="08404-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08404-114">PARAMETERS</span></span>

### <span data-ttu-id="08404-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="08404-115">-CdnOrigin</span></span>
<span data-ttu-id="08404-116">O objeto de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="08404-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="08404-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08404-117">-DefaultProfile</span></span>
<span data-ttu-id="08404-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="08404-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08404-119">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="08404-119">-EndpointName</span></span>
<span data-ttu-id="08404-120">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="08404-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="08404-121">-Nomedo Host</span><span class="sxs-lookup"><span data-stu-id="08404-121">-HostName</span></span>
<span data-ttu-id="08404-122">Nome do host de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="08404-122">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="08404-123">-httpPort</span><span class="sxs-lookup"><span data-stu-id="08404-123">-HttpPort</span></span>
<span data-ttu-id="08404-124">Porta http de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="08404-124">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="08404-125">-httpsPort</span><span class="sxs-lookup"><span data-stu-id="08404-125">-HttpsPort</span></span>
<span data-ttu-id="08404-126">Porta https de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="08404-126">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="08404-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="08404-127">-OriginHostHeader</span></span>
<span data-ttu-id="08404-128">Azure CDN origin host header.</span><span class="sxs-lookup"><span data-stu-id="08404-128">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="08404-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="08404-129">-OriginName</span></span>
<span data-ttu-id="08404-130">Nome de origem do CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="08404-130">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="08404-131">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="08404-131">-Priority</span></span>
<span data-ttu-id="08404-132">Prioridade de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="08404-132">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="08404-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="08404-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="08404-134">Uma mensagem personalizada a ser incluída na solicitação de aprovação para se conectar ao Link Particular.</span><span class="sxs-lookup"><span data-stu-id="08404-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="08404-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="08404-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="08404-136">Local do link particular de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="08404-136">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="08404-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="08404-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="08404-138">ID do recurso de link privado de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="08404-138">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="08404-139">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="08404-139">-ProfileName</span></span>
<span data-ttu-id="08404-140">Nome de perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="08404-140">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="08404-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08404-141">-ResourceGroupName</span></span>
<span data-ttu-id="08404-142">O grupo de recursos do perfil de CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="08404-142">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="08404-143">-Peso</span><span class="sxs-lookup"><span data-stu-id="08404-143">-Weight</span></span>
<span data-ttu-id="08404-144">Azure CDN origin weight.</span><span class="sxs-lookup"><span data-stu-id="08404-144">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="08404-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="08404-145">-Confirm</span></span>
<span data-ttu-id="08404-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08404-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08404-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08404-147">-WhatIf</span></span>
<span data-ttu-id="08404-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="08404-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08404-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08404-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08404-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08404-150">CommonParameters</span></span>
<span data-ttu-id="08404-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08404-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08404-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08404-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08404-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="08404-153">INPUTS</span></span>

### <span data-ttu-id="08404-154">Nenhum</span><span class="sxs-lookup"><span data-stu-id="08404-154">None</span></span>

## <span data-ttu-id="08404-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="08404-155">OUTPUTS</span></span>

### <span data-ttu-id="08404-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="08404-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="08404-157">Notas</span><span class="sxs-lookup"><span data-stu-id="08404-157">NOTES</span></span>

## <span data-ttu-id="08404-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08404-158">RELATED LINKS</span></span>
