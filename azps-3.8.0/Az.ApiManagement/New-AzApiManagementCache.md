---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: 4ae5bdd5dc9c15ab72b2f35f5d67eeaa732296bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942246"
---
# <span data-ttu-id="97bc0-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="97bc0-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="97bc0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="97bc0-103">Cria uma nova entidade de cache</span><span class="sxs-lookup"><span data-stu-id="97bc0-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="97bc0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97bc0-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97bc0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97bc0-105">DESCRIPTION</span></span>
<span data-ttu-id="97bc0-106">O cmdlet **New-AzApiManagementCache** cria uma nova entidade de cache no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="97bc0-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="97bc0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97bc0-107">EXAMPLES</span></span>

### <span data-ttu-id="97bc0-108">Exemplo 1: criar uma nova entidade de cache</span><span class="sxs-lookup"><span data-stu-id="97bc0-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="97bc0-109">Os cmdlets criam uma nova entidade de cache no local mestre do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="97bc0-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="97bc0-110">OS</span><span class="sxs-lookup"><span data-stu-id="97bc0-110">PARAMETERS</span></span>

### <span data-ttu-id="97bc0-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="97bc0-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="97bc0-112">Resourcebinding da instância de cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="97bc0-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="97bc0-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="97bc0-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="97bc0-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="97bc0-114">-CacheId</span></span>
<span data-ttu-id="97bc0-115">Identificador do novo cache.</span><span class="sxs-lookup"><span data-stu-id="97bc0-115">Identifier of new cache.</span></span>
<span data-ttu-id="97bc0-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="97bc0-116">This parameter is optional.</span></span>
<span data-ttu-id="97bc0-117">Se não for especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="97bc0-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="97bc0-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="97bc0-118">-ConnectionString</span></span>
<span data-ttu-id="97bc0-119">Cadeia de conexão Redis.</span><span class="sxs-lookup"><span data-stu-id="97bc0-119">Redis Connection String.</span></span>
<span data-ttu-id="97bc0-120">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="97bc0-120">This parameter is required.</span></span>

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

### <span data-ttu-id="97bc0-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="97bc0-121">-Context</span></span>
<span data-ttu-id="97bc0-122">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="97bc0-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="97bc0-123">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="97bc0-123">This parameter is required.</span></span>

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

### <span data-ttu-id="97bc0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97bc0-124">-DefaultProfile</span></span>
<span data-ttu-id="97bc0-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97bc0-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97bc0-126">-Descrição</span><span class="sxs-lookup"><span data-stu-id="97bc0-126">-Description</span></span>
<span data-ttu-id="97bc0-127">Descrição do cache.</span><span class="sxs-lookup"><span data-stu-id="97bc0-127">Cache Description.</span></span>
<span data-ttu-id="97bc0-128">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="97bc0-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="97bc0-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="97bc0-129">-Confirm</span></span>
<span data-ttu-id="97bc0-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97bc0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97bc0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97bc0-131">-WhatIf</span></span>
<span data-ttu-id="97bc0-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97bc0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97bc0-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97bc0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97bc0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97bc0-134">CommonParameters</span></span>
<span data-ttu-id="97bc0-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97bc0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97bc0-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97bc0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97bc0-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97bc0-137">INPUTS</span></span>

### <span data-ttu-id="97bc0-138">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="97bc0-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="97bc0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="97bc0-139">System.String</span></span>

## <span data-ttu-id="97bc0-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97bc0-140">OUTPUTS</span></span>

### <span data-ttu-id="97bc0-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="97bc0-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="97bc0-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97bc0-142">NOTES</span></span>

## <span data-ttu-id="97bc0-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97bc0-143">RELATED LINKS</span></span>

[<span data-ttu-id="97bc0-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="97bc0-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache)

[<span data-ttu-id="97bc0-145">Set-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="97bc0-145">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="97bc0-146">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="97bc0-146">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
