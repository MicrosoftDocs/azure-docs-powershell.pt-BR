---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 86eb7842bbd0dc29beb8572f4f34d53190ca06e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944159"
---
# <span data-ttu-id="ab261-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ab261-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="ab261-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab261-102">SYNOPSIS</span></span>
<span data-ttu-id="ab261-103">atualiza um cache no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="ab261-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="ab261-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab261-104">SYNTAX</span></span>

### <span data-ttu-id="ab261-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="ab261-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab261-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ab261-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab261-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ab261-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab261-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab261-108">DESCRIPTION</span></span>
<span data-ttu-id="ab261-109">O cmdlet **Update-AzApiManagementCache** atualiza um cache no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ab261-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="ab261-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab261-110">EXAMPLES</span></span>

### <span data-ttu-id="ab261-111">Exemplo 1: atualiza a descrição do cache em centralus</span><span class="sxs-lookup"><span data-stu-id="ab261-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
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

<span data-ttu-id="ab261-112">Atualiza a descrição do cache no centro dos EUA.</span><span class="sxs-lookup"><span data-stu-id="ab261-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="ab261-113">OS</span><span class="sxs-lookup"><span data-stu-id="ab261-113">PARAMETERS</span></span>

### <span data-ttu-id="ab261-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="ab261-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="ab261-115">Resourcebinding da instância de cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="ab261-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="ab261-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ab261-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab261-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="ab261-117">-CacheId</span></span>
<span data-ttu-id="ab261-118">Identificador do novo cache.</span><span class="sxs-lookup"><span data-stu-id="ab261-118">Identifier of new cache.</span></span>
<span data-ttu-id="ab261-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ab261-119">This parameter is required.</span></span>

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

### <span data-ttu-id="ab261-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="ab261-120">-ConnectionString</span></span>
<span data-ttu-id="ab261-121">Cadeia de conexão Redis.</span><span class="sxs-lookup"><span data-stu-id="ab261-121">Redis Connection String.</span></span>
<span data-ttu-id="ab261-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ab261-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab261-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ab261-123">-Context</span></span>
<span data-ttu-id="ab261-124">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ab261-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ab261-125">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ab261-125">This parameter is required.</span></span>

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

### <span data-ttu-id="ab261-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab261-126">-DefaultProfile</span></span>
<span data-ttu-id="ab261-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab261-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab261-128">-Descrição</span><span class="sxs-lookup"><span data-stu-id="ab261-128">-Description</span></span>
<span data-ttu-id="ab261-129">Descrição do cache.</span><span class="sxs-lookup"><span data-stu-id="ab261-129">Cache Description.</span></span>
<span data-ttu-id="ab261-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ab261-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab261-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab261-131">-InputObject</span></span>
<span data-ttu-id="ab261-132">Instância do PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="ab261-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="ab261-133">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ab261-133">This parameter is required.</span></span>

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

### <span data-ttu-id="ab261-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab261-134">-PassThru</span></span>
<span data-ttu-id="ab261-135">Se especificado, a instância do tipo Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCache que representa o cache modificado será gravada para output.</span><span class="sxs-lookup"><span data-stu-id="ab261-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="ab261-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab261-136">-ResourceId</span></span>
<span data-ttu-id="ab261-137">Resourcebinding do cache.</span><span class="sxs-lookup"><span data-stu-id="ab261-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="ab261-138">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ab261-138">This parameter is required.</span></span>

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

### <span data-ttu-id="ab261-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ab261-139">-Confirm</span></span>
<span data-ttu-id="ab261-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab261-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab261-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab261-141">-WhatIf</span></span>
<span data-ttu-id="ab261-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ab261-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab261-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ab261-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab261-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab261-144">CommonParameters</span></span>
<span data-ttu-id="ab261-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab261-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab261-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab261-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab261-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab261-147">INPUTS</span></span>

### <span data-ttu-id="ab261-148">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ab261-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ab261-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ab261-149">System.String</span></span>

### <span data-ttu-id="ab261-150">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ab261-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="ab261-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ab261-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ab261-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab261-152">OUTPUTS</span></span>

### <span data-ttu-id="ab261-153">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ab261-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="ab261-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab261-154">NOTES</span></span>

## <span data-ttu-id="ab261-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab261-155">RELATED LINKS</span></span>

[<span data-ttu-id="ab261-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ab261-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache)

[<span data-ttu-id="ab261-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ab261-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="ab261-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ab261-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)