---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: cfa2024064256b780121aeb489a3e8988b0a688e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115569"
---
# <span data-ttu-id="64539-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="64539-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="64539-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64539-102">SYNOPSIS</span></span>
<span data-ttu-id="64539-103">Cria uma nova entidade cache</span><span class="sxs-lookup"><span data-stu-id="64539-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="64539-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64539-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64539-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="64539-105">DESCRIPTION</span></span>
<span data-ttu-id="64539-106">O cmdlet **New-AzApiManagementCache** cria uma nova entidade de cache no serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="64539-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="64539-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="64539-107">EXAMPLES</span></span>

### <span data-ttu-id="64539-108">Exemplo 1: Criar uma nova entidade cache</span><span class="sxs-lookup"><span data-stu-id="64539-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="64539-109">Os cmdlets criam uma nova entidade de cache no local mestre do serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="64539-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="64539-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64539-110">PARAMETERS</span></span>

### <span data-ttu-id="64539-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="64539-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="64539-112">Arm ResourceId da instância do Cache de Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="64539-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="64539-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="64539-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="64539-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="64539-114">-CacheId</span></span>
<span data-ttu-id="64539-115">Identificador do novo cache.</span><span class="sxs-lookup"><span data-stu-id="64539-115">Identifier of new cache.</span></span>
<span data-ttu-id="64539-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="64539-116">This parameter is optional.</span></span>
<span data-ttu-id="64539-117">Se não especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="64539-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="64539-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="64539-118">-ConnectionString</span></span>
<span data-ttu-id="64539-119">Redis Connection String.</span><span class="sxs-lookup"><span data-stu-id="64539-119">Redis Connection String.</span></span>
<span data-ttu-id="64539-120">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="64539-120">This parameter is required.</span></span>

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

### <span data-ttu-id="64539-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="64539-121">-Context</span></span>
<span data-ttu-id="64539-122">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="64539-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="64539-123">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="64539-123">This parameter is required.</span></span>

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

### <span data-ttu-id="64539-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64539-124">-DefaultProfile</span></span>
<span data-ttu-id="64539-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64539-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64539-126">-Descrição</span><span class="sxs-lookup"><span data-stu-id="64539-126">-Description</span></span>
<span data-ttu-id="64539-127">Descrição do Cache.</span><span class="sxs-lookup"><span data-stu-id="64539-127">Cache Description.</span></span>
<span data-ttu-id="64539-128">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="64539-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="64539-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="64539-129">-Confirm</span></span>
<span data-ttu-id="64539-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64539-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64539-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64539-131">-WhatIf</span></span>
<span data-ttu-id="64539-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="64539-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64539-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64539-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64539-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64539-134">CommonParameters</span></span>
<span data-ttu-id="64539-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64539-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64539-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64539-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64539-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="64539-137">INPUTS</span></span>

### <span data-ttu-id="64539-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="64539-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="64539-139">System.String</span><span class="sxs-lookup"><span data-stu-id="64539-139">System.String</span></span>

## <span data-ttu-id="64539-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="64539-140">OUTPUTS</span></span>

### <span data-ttu-id="64539-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="64539-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="64539-142">Notas</span><span class="sxs-lookup"><span data-stu-id="64539-142">NOTES</span></span>

## <span data-ttu-id="64539-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64539-143">RELATED LINKS</span></span>

[<span data-ttu-id="64539-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="64539-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="64539-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="64539-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="64539-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="64539-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
