---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: cfa2024064256b780121aeb489a3e8988b0a688e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256596"
---
# <span data-ttu-id="0cee9-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="0cee9-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="0cee9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0cee9-102">SYNOPSIS</span></span>
<span data-ttu-id="0cee9-103">Cria uma nova entidade de cache</span><span class="sxs-lookup"><span data-stu-id="0cee9-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="0cee9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0cee9-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cee9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0cee9-105">DESCRIPTION</span></span>
<span data-ttu-id="0cee9-106">O cmdlet **New-AzApiManagementCache** cria uma nova entidade de cache no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="0cee9-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="0cee9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0cee9-107">EXAMPLES</span></span>

### <span data-ttu-id="0cee9-108">Exemplo 1: criar uma nova entidade de cache</span><span class="sxs-lookup"><span data-stu-id="0cee9-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="0cee9-109">Os cmdlets criam uma nova entidade de cache no local mestre do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="0cee9-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="0cee9-110">OS</span><span class="sxs-lookup"><span data-stu-id="0cee9-110">PARAMETERS</span></span>

### <span data-ttu-id="0cee9-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="0cee9-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="0cee9-112">Resourcebinding da instância de cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="0cee9-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="0cee9-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0cee9-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="0cee9-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="0cee9-114">-CacheId</span></span>
<span data-ttu-id="0cee9-115">Identificador do novo cache.</span><span class="sxs-lookup"><span data-stu-id="0cee9-115">Identifier of new cache.</span></span>
<span data-ttu-id="0cee9-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0cee9-116">This parameter is optional.</span></span>
<span data-ttu-id="0cee9-117">Se não for especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="0cee9-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="0cee9-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="0cee9-118">-ConnectionString</span></span>
<span data-ttu-id="0cee9-119">Cadeia de conexão Redis.</span><span class="sxs-lookup"><span data-stu-id="0cee9-119">Redis Connection String.</span></span>
<span data-ttu-id="0cee9-120">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0cee9-120">This parameter is required.</span></span>

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

### <span data-ttu-id="0cee9-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="0cee9-121">-Context</span></span>
<span data-ttu-id="0cee9-122">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0cee9-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0cee9-123">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0cee9-123">This parameter is required.</span></span>

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

### <span data-ttu-id="0cee9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cee9-124">-DefaultProfile</span></span>
<span data-ttu-id="0cee9-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0cee9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cee9-126">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0cee9-126">-Description</span></span>
<span data-ttu-id="0cee9-127">Descrição do cache.</span><span class="sxs-lookup"><span data-stu-id="0cee9-127">Cache Description.</span></span>
<span data-ttu-id="0cee9-128">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0cee9-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="0cee9-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0cee9-129">-Confirm</span></span>
<span data-ttu-id="0cee9-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cee9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cee9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cee9-131">-WhatIf</span></span>
<span data-ttu-id="0cee9-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0cee9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cee9-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0cee9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cee9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cee9-134">CommonParameters</span></span>
<span data-ttu-id="0cee9-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cee9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cee9-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0cee9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cee9-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0cee9-137">INPUTS</span></span>

### <span data-ttu-id="0cee9-138">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0cee9-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0cee9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0cee9-139">System.String</span></span>

## <span data-ttu-id="0cee9-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0cee9-140">OUTPUTS</span></span>

### <span data-ttu-id="0cee9-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="0cee9-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="0cee9-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0cee9-142">NOTES</span></span>

## <span data-ttu-id="0cee9-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0cee9-143">RELATED LINKS</span></span>

[<span data-ttu-id="0cee9-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="0cee9-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="0cee9-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="0cee9-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="0cee9-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="0cee9-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
