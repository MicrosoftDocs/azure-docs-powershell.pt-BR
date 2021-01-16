---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: a9ef1687333851e2ac67dfb3f0146509f3b77183
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430331"
---
# <span data-ttu-id="6ab59-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="6ab59-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="6ab59-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ab59-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab59-103">Cria uma nova origem CDN</span><span class="sxs-lookup"><span data-stu-id="6ab59-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="6ab59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ab59-104">SYNTAX</span></span>

### <span data-ttu-id="6ab59-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6ab59-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ab59-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ab59-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ab59-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ab59-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ab59-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ab59-108">DESCRIPTION</span></span>
<span data-ttu-id="6ab59-109">O New-AzCdnOrigin criará uma nova origem CDN no ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="6ab59-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="6ab59-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ab59-110">EXAMPLES</span></span>

### <span data-ttu-id="6ab59-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6ab59-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="6ab59-112">Esse cmdlet criará uma nova origem CDN para o ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="6ab59-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="6ab59-113">Ele usará o nome do host fornecido como origem.</span><span class="sxs-lookup"><span data-stu-id="6ab59-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="6ab59-114">OS</span><span class="sxs-lookup"><span data-stu-id="6ab59-114">PARAMETERS</span></span>

### <span data-ttu-id="6ab59-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="6ab59-115">-CdnOrigin</span></span>
<span data-ttu-id="6ab59-116">O objeto de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="6ab59-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="6ab59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab59-117">-DefaultProfile</span></span>
<span data-ttu-id="6ab59-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab59-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ab59-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6ab59-119">-EndpointName</span></span>
<span data-ttu-id="6ab59-120">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab59-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="6ab59-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="6ab59-121">-HostName</span></span>
<span data-ttu-id="6ab59-122">Nome do host da origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab59-122">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="6ab59-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="6ab59-123">-HttpPort</span></span>
<span data-ttu-id="6ab59-124">Porta http da origem CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab59-124">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="6ab59-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="6ab59-125">-HttpsPort</span></span>
<span data-ttu-id="6ab59-126">Porta https da origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab59-126">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="6ab59-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="6ab59-127">-OriginHostHeader</span></span>
<span data-ttu-id="6ab59-128">Cabeçalho do host de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab59-128">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="6ab59-129">-Originname</span><span class="sxs-lookup"><span data-stu-id="6ab59-129">-OriginName</span></span>
<span data-ttu-id="6ab59-130">Nome da origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab59-130">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="6ab59-131">-Priority</span><span class="sxs-lookup"><span data-stu-id="6ab59-131">-Priority</span></span>
<span data-ttu-id="6ab59-132">Prioridade de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab59-132">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="6ab59-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="6ab59-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="6ab59-134">Uma mensagem personalizada a ser incluída na solicitação de aprovação para se conectar ao link particular.</span><span class="sxs-lookup"><span data-stu-id="6ab59-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="6ab59-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="6ab59-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="6ab59-136">Local do link particular de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab59-136">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="6ab59-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="6ab59-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="6ab59-138">ID do recurso do link privado da origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab59-138">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="6ab59-139">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6ab59-139">-ProfileName</span></span>
<span data-ttu-id="6ab59-140">Nome do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab59-140">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="6ab59-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ab59-141">-ResourceGroupName</span></span>
<span data-ttu-id="6ab59-142">O grupo de recursos do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab59-142">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="6ab59-143">-Weight</span><span class="sxs-lookup"><span data-stu-id="6ab59-143">-Weight</span></span>
<span data-ttu-id="6ab59-144">Peso da origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab59-144">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="6ab59-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6ab59-145">-Confirm</span></span>
<span data-ttu-id="6ab59-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ab59-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ab59-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ab59-147">-WhatIf</span></span>
<span data-ttu-id="6ab59-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6ab59-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ab59-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6ab59-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ab59-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab59-150">CommonParameters</span></span>
<span data-ttu-id="6ab59-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab59-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab59-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ab59-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab59-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ab59-153">INPUTS</span></span>

### <span data-ttu-id="6ab59-154">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6ab59-154">None</span></span>

## <span data-ttu-id="6ab59-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ab59-155">OUTPUTS</span></span>

### <span data-ttu-id="6ab59-156">Microsoft. Azure. Commands. cdn. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="6ab59-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="6ab59-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ab59-157">NOTES</span></span>

## <span data-ttu-id="6ab59-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ab59-158">RELATED LINKS</span></span>
