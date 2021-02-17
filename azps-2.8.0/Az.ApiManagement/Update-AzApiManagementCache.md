---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: c8c535168a86607daab27ab89340d231bb4e4bd3
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406886"
---
# <span data-ttu-id="3ad54-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="3ad54-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="3ad54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ad54-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad54-103">atualiza um cache no serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="3ad54-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="3ad54-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ad54-104">SYNTAX</span></span>

### <span data-ttu-id="3ad54-105">ExpandedParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3ad54-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ad54-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3ad54-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ad54-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ad54-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ad54-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ad54-108">DESCRIPTION</span></span>
<span data-ttu-id="3ad54-109">O cmdlet **Update-AzApiManagementCache** atualiza um cache no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3ad54-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="3ad54-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3ad54-110">EXAMPLES</span></span>

### <span data-ttu-id="3ad54-111">Exemplo 1: atualiza a Descrição do Cache no centro</span><span class="sxs-lookup"><span data-stu-id="3ad54-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
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

<span data-ttu-id="3ad54-112">Atualiza a descrição do Cache na Central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="3ad54-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="3ad54-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ad54-113">PARAMETERS</span></span>

### <span data-ttu-id="3ad54-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="3ad54-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="3ad54-115">Arm ResourceId da instância do Cache de Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad54-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="3ad54-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="3ad54-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="3ad54-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="3ad54-117">-CacheId</span></span>
<span data-ttu-id="3ad54-118">Identificador do novo cache.</span><span class="sxs-lookup"><span data-stu-id="3ad54-118">Identifier of new cache.</span></span>
<span data-ttu-id="3ad54-119">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3ad54-119">This parameter is required.</span></span>

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

### <span data-ttu-id="3ad54-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="3ad54-120">-ConnectionString</span></span>
<span data-ttu-id="3ad54-121">Redis Connection String.</span><span class="sxs-lookup"><span data-stu-id="3ad54-121">Redis Connection String.</span></span>
<span data-ttu-id="3ad54-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="3ad54-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="3ad54-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3ad54-123">-Context</span></span>
<span data-ttu-id="3ad54-124">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3ad54-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3ad54-125">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3ad54-125">This parameter is required.</span></span>

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

### <span data-ttu-id="3ad54-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ad54-126">-DefaultProfile</span></span>
<span data-ttu-id="3ad54-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad54-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ad54-128">-Descrição</span><span class="sxs-lookup"><span data-stu-id="3ad54-128">-Description</span></span>
<span data-ttu-id="3ad54-129">Descrição do Cache.</span><span class="sxs-lookup"><span data-stu-id="3ad54-129">Cache Description.</span></span>
<span data-ttu-id="3ad54-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="3ad54-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="3ad54-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ad54-131">-InputObject</span></span>
<span data-ttu-id="3ad54-132">Instância de PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="3ad54-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="3ad54-133">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3ad54-133">This parameter is required.</span></span>

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

### <span data-ttu-id="3ad54-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ad54-134">-PassThru</span></span>
<span data-ttu-id="3ad54-135">Se especificado, a instância do Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache que representa o cache modificado será escrita na saída.</span><span class="sxs-lookup"><span data-stu-id="3ad54-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="3ad54-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ad54-136">-ResourceId</span></span>
<span data-ttu-id="3ad54-137">Arm ResourceId of Cache.</span><span class="sxs-lookup"><span data-stu-id="3ad54-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="3ad54-138">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3ad54-138">This parameter is required.</span></span>

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

### <span data-ttu-id="3ad54-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3ad54-139">-Confirm</span></span>
<span data-ttu-id="3ad54-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ad54-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ad54-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ad54-141">-WhatIf</span></span>
<span data-ttu-id="3ad54-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3ad54-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ad54-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ad54-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ad54-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad54-144">CommonParameters</span></span>
<span data-ttu-id="3ad54-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ad54-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad54-146">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ad54-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad54-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="3ad54-147">INPUTS</span></span>

### <span data-ttu-id="3ad54-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3ad54-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3ad54-149">System.String</span><span class="sxs-lookup"><span data-stu-id="3ad54-149">System.String</span></span>

### <span data-ttu-id="3ad54-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="3ad54-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="3ad54-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3ad54-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3ad54-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="3ad54-152">OUTPUTS</span></span>

### <span data-ttu-id="3ad54-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="3ad54-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="3ad54-154">Notas</span><span class="sxs-lookup"><span data-stu-id="3ad54-154">NOTES</span></span>

## <span data-ttu-id="3ad54-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ad54-155">RELATED LINKS</span></span>

[<span data-ttu-id="3ad54-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="3ad54-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="3ad54-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="3ad54-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="3ad54-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="3ad54-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
