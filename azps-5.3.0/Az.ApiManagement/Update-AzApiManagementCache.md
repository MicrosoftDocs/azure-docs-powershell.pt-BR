---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 2ac2eb7cb40cb7df4324aff276137527d4b148a5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272087"
---
# <span data-ttu-id="2f00a-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="2f00a-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="2f00a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f00a-102">SYNOPSIS</span></span>
<span data-ttu-id="2f00a-103">atualiza um cache no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2f00a-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="2f00a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f00a-104">SYNTAX</span></span>

### <span data-ttu-id="2f00a-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="2f00a-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f00a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2f00a-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f00a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f00a-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f00a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f00a-108">DESCRIPTION</span></span>
<span data-ttu-id="2f00a-109">O cmdlet **Update-AzApiManagementCache** atualiza um cache no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2f00a-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="2f00a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f00a-110">EXAMPLES</span></span>

### <span data-ttu-id="2f00a-111">Exemplo 1: atualiza a descrição do cache em centralus</span><span class="sxs-lookup"><span data-stu-id="2f00a-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
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

<span data-ttu-id="2f00a-112">Atualiza a descrição do cache no centro dos EUA.</span><span class="sxs-lookup"><span data-stu-id="2f00a-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="2f00a-113">OS</span><span class="sxs-lookup"><span data-stu-id="2f00a-113">PARAMETERS</span></span>

### <span data-ttu-id="2f00a-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="2f00a-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="2f00a-115">Resourcebinding da instância de cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="2f00a-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="2f00a-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="2f00a-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="2f00a-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="2f00a-117">-CacheId</span></span>
<span data-ttu-id="2f00a-118">Identificador do novo cache.</span><span class="sxs-lookup"><span data-stu-id="2f00a-118">Identifier of new cache.</span></span>
<span data-ttu-id="2f00a-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2f00a-119">This parameter is required.</span></span>

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

### <span data-ttu-id="2f00a-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="2f00a-120">-ConnectionString</span></span>
<span data-ttu-id="2f00a-121">Cadeia de conexão Redis.</span><span class="sxs-lookup"><span data-stu-id="2f00a-121">Redis Connection String.</span></span>
<span data-ttu-id="2f00a-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="2f00a-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="2f00a-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2f00a-123">-Context</span></span>
<span data-ttu-id="2f00a-124">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2f00a-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2f00a-125">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2f00a-125">This parameter is required.</span></span>

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

### <span data-ttu-id="2f00a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f00a-126">-DefaultProfile</span></span>
<span data-ttu-id="2f00a-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f00a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f00a-128">-Descrição</span><span class="sxs-lookup"><span data-stu-id="2f00a-128">-Description</span></span>
<span data-ttu-id="2f00a-129">Descrição do cache.</span><span class="sxs-lookup"><span data-stu-id="2f00a-129">Cache Description.</span></span>
<span data-ttu-id="2f00a-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="2f00a-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="2f00a-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f00a-131">-InputObject</span></span>
<span data-ttu-id="2f00a-132">Instância do PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="2f00a-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="2f00a-133">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2f00a-133">This parameter is required.</span></span>

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

### <span data-ttu-id="2f00a-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f00a-134">-PassThru</span></span>
<span data-ttu-id="2f00a-135">Se especificado, a instância do tipo Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCache que representa o cache modificado será gravada para output.</span><span class="sxs-lookup"><span data-stu-id="2f00a-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="2f00a-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f00a-136">-ResourceId</span></span>
<span data-ttu-id="2f00a-137">Resourcebinding do cache.</span><span class="sxs-lookup"><span data-stu-id="2f00a-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="2f00a-138">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2f00a-138">This parameter is required.</span></span>

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

### <span data-ttu-id="2f00a-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2f00a-139">-Confirm</span></span>
<span data-ttu-id="2f00a-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f00a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f00a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f00a-141">-WhatIf</span></span>
<span data-ttu-id="2f00a-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2f00a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f00a-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f00a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f00a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f00a-144">CommonParameters</span></span>
<span data-ttu-id="2f00a-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f00a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f00a-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f00a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f00a-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f00a-147">INPUTS</span></span>

### <span data-ttu-id="2f00a-148">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2f00a-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2f00a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="2f00a-149">System.String</span></span>

### <span data-ttu-id="2f00a-150">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="2f00a-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="2f00a-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2f00a-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2f00a-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f00a-152">OUTPUTS</span></span>

### <span data-ttu-id="2f00a-153">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="2f00a-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="2f00a-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f00a-154">NOTES</span></span>

## <span data-ttu-id="2f00a-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f00a-155">RELATED LINKS</span></span>

[<span data-ttu-id="2f00a-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="2f00a-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="2f00a-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="2f00a-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="2f00a-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="2f00a-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
