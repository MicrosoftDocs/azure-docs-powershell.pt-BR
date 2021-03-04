---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: 13fe16c2612a267df0760aad939b46e427d6fab1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886499"
---
# <span data-ttu-id="211b1-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="211b1-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="211b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="211b1-102">SYNOPSIS</span></span>
<span data-ttu-id="211b1-103">Cria uma nova entidade Cache</span><span class="sxs-lookup"><span data-stu-id="211b1-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="211b1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="211b1-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="211b1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="211b1-105">DESCRIPTION</span></span>
<span data-ttu-id="211b1-106">O cmdlet **New-AzApiManagementCache** cria uma nova entidade de cache no serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="211b1-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="211b1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="211b1-107">EXAMPLES</span></span>

### <span data-ttu-id="211b1-108">Exemplo 1 : Criar uma nova entidade cache</span><span class="sxs-lookup"><span data-stu-id="211b1-108">Example 1 : Create a new Cache entity</span></span>
```powershell
PS c:\> New-AzApiManagementCache -Context $context -ConnectionString "teamdemo.redis.cache.windows.net:6380,password=xxxxxx+xxxxx=,ssl=True,abortConnect=False" -Description "Team Cache"

CacheId           : centralus
Description       : Team Cache
ConnectionString  : {{5cc19889e6ed3b0524c3f7d3}}
ResourceId        :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsof
                    t.ApiManagement/service/contoso/caches/centralus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="211b1-109">Os cmdlets criam uma nova entidade de cache na localização mestra do serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="211b1-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="211b1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="211b1-110">PARAMETERS</span></span>

### <span data-ttu-id="211b1-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="211b1-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="211b1-112">Arm ResourceId da instância cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="211b1-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="211b1-113">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="211b1-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="211b1-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="211b1-114">-CacheId</span></span>
<span data-ttu-id="211b1-115">Identificador do novo cache.</span><span class="sxs-lookup"><span data-stu-id="211b1-115">Identifier of new cache.</span></span>
<span data-ttu-id="211b1-116">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="211b1-116">This parameter is optional.</span></span>
<span data-ttu-id="211b1-117">Se não for especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="211b1-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="211b1-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="211b1-118">-ConnectionString</span></span>
<span data-ttu-id="211b1-119">Redis Connection String.</span><span class="sxs-lookup"><span data-stu-id="211b1-119">Redis Connection String.</span></span>
<span data-ttu-id="211b1-120">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="211b1-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="211b1-121">-Context</span><span class="sxs-lookup"><span data-stu-id="211b1-121">-Context</span></span>
<span data-ttu-id="211b1-122">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="211b1-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="211b1-123">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="211b1-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="211b1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="211b1-124">-DefaultProfile</span></span>
<span data-ttu-id="211b1-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="211b1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="211b1-126">-Description</span><span class="sxs-lookup"><span data-stu-id="211b1-126">-Description</span></span>
<span data-ttu-id="211b1-127">Descrição do cache.</span><span class="sxs-lookup"><span data-stu-id="211b1-127">Cache Description.</span></span>
<span data-ttu-id="211b1-128">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="211b1-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="211b1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="211b1-129">-Confirm</span></span>
<span data-ttu-id="211b1-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="211b1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="211b1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="211b1-131">-WhatIf</span></span>
<span data-ttu-id="211b1-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="211b1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="211b1-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="211b1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="211b1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="211b1-134">CommonParameters</span></span>
<span data-ttu-id="211b1-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="211b1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="211b1-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="211b1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="211b1-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="211b1-137">INPUTS</span></span>

### <span data-ttu-id="211b1-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="211b1-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="211b1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="211b1-139">System.String</span></span>

## <span data-ttu-id="211b1-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="211b1-140">OUTPUTS</span></span>

### <span data-ttu-id="211b1-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="211b1-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="211b1-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="211b1-142">NOTES</span></span>

## <span data-ttu-id="211b1-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="211b1-143">RELATED LINKS</span></span>

[<span data-ttu-id="211b1-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="211b1-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="211b1-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="211b1-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="211b1-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="211b1-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
