---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 8c7b423090de10ea1573d268dcc3c301ec4b206d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891895"
---
# <span data-ttu-id="e4df7-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e4df7-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="e4df7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4df7-102">SYNOPSIS</span></span>
<span data-ttu-id="e4df7-103">atualiza um cache no serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="e4df7-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="e4df7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e4df7-104">SYNTAX</span></span>

### <span data-ttu-id="e4df7-105">ExpandedParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e4df7-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4df7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e4df7-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4df7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e4df7-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4df7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e4df7-108">DESCRIPTION</span></span>
<span data-ttu-id="e4df7-109">O cmdlet **Update-AzApiManagementCache** atualiza um cache no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e4df7-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="e4df7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4df7-110">EXAMPLES</span></span>

### <span data-ttu-id="e4df7-111">Exemplo 1 : atualiza a Descrição do Cache em centralus</span><span class="sxs-lookup"><span data-stu-id="e4df7-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
```powershell
PS D:\github\azure-powershell> $context=New-AzApiManagementContext -ResourceGroupName Api-Default-Central-US -ServiceName contoso
PS D:\github\azure-powershell> Update-AzApiManagementCache -Context $context -CacheId centralus -Description "Team new cache" -PassThru


CacheId              : centralus
Description          : Team new cache
ConnectionString     : {{5cc19889e6ed3b0524c3f7d3}}
AzureRedisResourceId :
Id                   : /subscriptions/subid/resourceGroups/Api-Default-Central-US/providers/M
                       icrosoft.ApiManagement/service/contoso/caches/centralus
ResourceGroupName    : Api-Default-Central-US
ServiceName          : contoso
```

<span data-ttu-id="e4df7-112">Atualiza a descrição do Cache no Central US.</span><span class="sxs-lookup"><span data-stu-id="e4df7-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="e4df7-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e4df7-113">PARAMETERS</span></span>

### <span data-ttu-id="e4df7-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="e4df7-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="e4df7-115">Arm ResourceId da instância cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="e4df7-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="e4df7-116">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e4df7-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4df7-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="e4df7-117">-CacheId</span></span>
<span data-ttu-id="e4df7-118">Identificador do novo cache.</span><span class="sxs-lookup"><span data-stu-id="e4df7-118">Identifier of new cache.</span></span>
<span data-ttu-id="e4df7-119">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e4df7-119">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4df7-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e4df7-120">-ConnectionString</span></span>
<span data-ttu-id="e4df7-121">Redis Connection String.</span><span class="sxs-lookup"><span data-stu-id="e4df7-121">Redis Connection String.</span></span>
<span data-ttu-id="e4df7-122">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e4df7-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4df7-123">-Context</span><span class="sxs-lookup"><span data-stu-id="e4df7-123">-Context</span></span>
<span data-ttu-id="e4df7-124">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e4df7-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e4df7-125">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e4df7-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4df7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4df7-126">-DefaultProfile</span></span>
<span data-ttu-id="e4df7-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4df7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4df7-128">-Description</span><span class="sxs-lookup"><span data-stu-id="e4df7-128">-Description</span></span>
<span data-ttu-id="e4df7-129">Descrição do cache.</span><span class="sxs-lookup"><span data-stu-id="e4df7-129">Cache Description.</span></span>
<span data-ttu-id="e4df7-130">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e4df7-130">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4df7-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4df7-131">-InputObject</span></span>
<span data-ttu-id="e4df7-132">Instância de PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="e4df7-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="e4df7-133">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e4df7-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4df7-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4df7-134">-PassThru</span></span>
<span data-ttu-id="e4df7-135">Se especificado, a instância do Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache tipo que representa o cache modificado será gravado na saída.</span><span class="sxs-lookup"><span data-stu-id="e4df7-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4df7-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4df7-136">-ResourceId</span></span>
<span data-ttu-id="e4df7-137">Arm ResourceId de Cache.</span><span class="sxs-lookup"><span data-stu-id="e4df7-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="e4df7-138">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e4df7-138">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4df7-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4df7-139">-Confirm</span></span>
<span data-ttu-id="e4df7-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4df7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4df7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4df7-141">-WhatIf</span></span>
<span data-ttu-id="e4df7-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4df7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4df7-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4df7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4df7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4df7-144">CommonParameters</span></span>
<span data-ttu-id="e4df7-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4df7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4df7-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4df7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4df7-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4df7-147">INPUTS</span></span>

### <span data-ttu-id="e4df7-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e4df7-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e4df7-149">System.String</span><span class="sxs-lookup"><span data-stu-id="e4df7-149">System.String</span></span>

### <span data-ttu-id="e4df7-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e4df7-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="e4df7-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e4df7-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e4df7-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e4df7-152">OUTPUTS</span></span>

### <span data-ttu-id="e4df7-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e4df7-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="e4df7-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="e4df7-154">NOTES</span></span>

## <span data-ttu-id="e4df7-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4df7-155">RELATED LINKS</span></span>

[<span data-ttu-id="e4df7-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e4df7-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="e4df7-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e4df7-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="e4df7-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e4df7-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
