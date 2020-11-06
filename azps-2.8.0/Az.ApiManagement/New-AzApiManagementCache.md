---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: 90da707ce34c191a33a68473f41555a33c0e35b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598056"
---
# <span data-ttu-id="ba009-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ba009-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="ba009-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba009-102">SYNOPSIS</span></span>
<span data-ttu-id="ba009-103">Cria uma nova entidade de cache</span><span class="sxs-lookup"><span data-stu-id="ba009-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="ba009-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba009-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba009-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba009-105">DESCRIPTION</span></span>
<span data-ttu-id="ba009-106">O cmdlet **New-AzApiManagementCache** cria uma nova entidade de cache no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="ba009-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="ba009-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba009-107">EXAMPLES</span></span>

### <span data-ttu-id="ba009-108">Exemplo 1: criar uma nova entidade de cache</span><span class="sxs-lookup"><span data-stu-id="ba009-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="ba009-109">Os cmdlets criam uma nova entidade de cache no local mestre do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="ba009-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="ba009-110">OS</span><span class="sxs-lookup"><span data-stu-id="ba009-110">PARAMETERS</span></span>

### <span data-ttu-id="ba009-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="ba009-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="ba009-112">Resourcebinding da instância de cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="ba009-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="ba009-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ba009-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="ba009-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="ba009-114">-CacheId</span></span>
<span data-ttu-id="ba009-115">Identificador do novo cache.</span><span class="sxs-lookup"><span data-stu-id="ba009-115">Identifier of new cache.</span></span>
<span data-ttu-id="ba009-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ba009-116">This parameter is optional.</span></span>
<span data-ttu-id="ba009-117">Se não for especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="ba009-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="ba009-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="ba009-118">-ConnectionString</span></span>
<span data-ttu-id="ba009-119">Cadeia de conexão Redis.</span><span class="sxs-lookup"><span data-stu-id="ba009-119">Redis Connection String.</span></span>
<span data-ttu-id="ba009-120">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ba009-120">This parameter is required.</span></span>

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

### <span data-ttu-id="ba009-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ba009-121">-Context</span></span>
<span data-ttu-id="ba009-122">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ba009-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ba009-123">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ba009-123">This parameter is required.</span></span>

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

### <span data-ttu-id="ba009-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba009-124">-DefaultProfile</span></span>
<span data-ttu-id="ba009-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba009-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba009-126">-Descrição</span><span class="sxs-lookup"><span data-stu-id="ba009-126">-Description</span></span>
<span data-ttu-id="ba009-127">Descrição do cache.</span><span class="sxs-lookup"><span data-stu-id="ba009-127">Cache Description.</span></span>
<span data-ttu-id="ba009-128">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ba009-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="ba009-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ba009-129">-Confirm</span></span>
<span data-ttu-id="ba009-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba009-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba009-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba009-131">-WhatIf</span></span>
<span data-ttu-id="ba009-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ba009-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba009-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ba009-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba009-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba009-134">CommonParameters</span></span>
<span data-ttu-id="ba009-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba009-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba009-136">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba009-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba009-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba009-137">INPUTS</span></span>

### <span data-ttu-id="ba009-138">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ba009-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ba009-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ba009-139">System.String</span></span>

## <span data-ttu-id="ba009-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba009-140">OUTPUTS</span></span>

### <span data-ttu-id="ba009-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ba009-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="ba009-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba009-142">NOTES</span></span>

## <span data-ttu-id="ba009-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba009-143">RELATED LINKS</span></span>

[<span data-ttu-id="ba009-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ba009-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache)

[<span data-ttu-id="ba009-145">Set-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ba009-145">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="ba009-146">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ba009-146">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
