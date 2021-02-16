---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: cfa2024064256b780121aeb489a3e8988b0a688e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398097"
---
# <span data-ttu-id="c7a57-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c7a57-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="c7a57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7a57-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a57-103">Cria uma nova entidade cache</span><span class="sxs-lookup"><span data-stu-id="c7a57-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="c7a57-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7a57-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7a57-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7a57-105">DESCRIPTION</span></span>
<span data-ttu-id="c7a57-106">O cmdlet **New-AzApiManagementCache** cria uma nova entidade de cache no serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="c7a57-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="c7a57-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c7a57-107">EXAMPLES</span></span>

### <span data-ttu-id="c7a57-108">Exemplo 1: Criar uma nova entidade cache</span><span class="sxs-lookup"><span data-stu-id="c7a57-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="c7a57-109">Os cmdlets criam uma nova entidade de cache no local mestre do serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="c7a57-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="c7a57-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7a57-110">PARAMETERS</span></span>

### <span data-ttu-id="c7a57-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="c7a57-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="c7a57-112">Arm ResourceId da instância do Cache de Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a57-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="c7a57-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c7a57-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7a57-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="c7a57-114">-CacheId</span></span>
<span data-ttu-id="c7a57-115">Identificador do novo cache.</span><span class="sxs-lookup"><span data-stu-id="c7a57-115">Identifier of new cache.</span></span>
<span data-ttu-id="c7a57-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c7a57-116">This parameter is optional.</span></span>
<span data-ttu-id="c7a57-117">Se não especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="c7a57-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="c7a57-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="c7a57-118">-ConnectionString</span></span>
<span data-ttu-id="c7a57-119">Redis Connection String.</span><span class="sxs-lookup"><span data-stu-id="c7a57-119">Redis Connection String.</span></span>
<span data-ttu-id="c7a57-120">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c7a57-120">This parameter is required.</span></span>

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

### <span data-ttu-id="c7a57-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c7a57-121">-Context</span></span>
<span data-ttu-id="c7a57-122">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c7a57-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c7a57-123">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c7a57-123">This parameter is required.</span></span>

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

### <span data-ttu-id="c7a57-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a57-124">-DefaultProfile</span></span>
<span data-ttu-id="c7a57-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a57-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7a57-126">-Descrição</span><span class="sxs-lookup"><span data-stu-id="c7a57-126">-Description</span></span>
<span data-ttu-id="c7a57-127">Descrição do Cache.</span><span class="sxs-lookup"><span data-stu-id="c7a57-127">Cache Description.</span></span>
<span data-ttu-id="c7a57-128">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c7a57-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7a57-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c7a57-129">-Confirm</span></span>
<span data-ttu-id="c7a57-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7a57-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7a57-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7a57-131">-WhatIf</span></span>
<span data-ttu-id="c7a57-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c7a57-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7a57-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c7a57-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7a57-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a57-134">CommonParameters</span></span>
<span data-ttu-id="c7a57-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a57-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a57-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7a57-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a57-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="c7a57-137">INPUTS</span></span>

### <span data-ttu-id="c7a57-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c7a57-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c7a57-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c7a57-139">System.String</span></span>

## <span data-ttu-id="c7a57-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="c7a57-140">OUTPUTS</span></span>

### <span data-ttu-id="c7a57-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c7a57-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="c7a57-142">Notas</span><span class="sxs-lookup"><span data-stu-id="c7a57-142">NOTES</span></span>

## <span data-ttu-id="c7a57-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7a57-143">RELATED LINKS</span></span>

[<span data-ttu-id="c7a57-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c7a57-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="c7a57-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c7a57-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="c7a57-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c7a57-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
