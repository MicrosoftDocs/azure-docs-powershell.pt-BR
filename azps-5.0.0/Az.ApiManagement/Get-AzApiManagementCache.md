---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: fee978a1500c0fc472ec8015a3e8dbbbdc8015bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125073"
---
# <span data-ttu-id="47af5-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="47af5-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="47af5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47af5-102">SYNOPSIS</span></span>
<span data-ttu-id="47af5-103">Obtenha os detalhes do cache.</span><span class="sxs-lookup"><span data-stu-id="47af5-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="47af5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47af5-104">SYNTAX</span></span>

### <span data-ttu-id="47af5-105">ContextParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="47af5-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47af5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47af5-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47af5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47af5-107">DESCRIPTION</span></span>
<span data-ttu-id="47af5-108">Obtenha os detalhes do cache configurado no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="47af5-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="47af5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47af5-109">EXAMPLES</span></span>

### <span data-ttu-id="47af5-110">Exemplo 1: obter todos os caches</span><span class="sxs-lookup"><span data-stu-id="47af5-110">Example 1: Get all Caches</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-West-US
ServiceName       : contoso
```

<span data-ttu-id="47af5-111">Obtém uma lista de todos os caches configurados no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="47af5-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="47af5-112">Exemplo 2: obter o cache especificado pelo identificador westus</span><span class="sxs-lookup"><span data-stu-id="47af5-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext -cacheId westus
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="47af5-113">Obter os detalhes do cache especificado configurado para oesteus</span><span class="sxs-lookup"><span data-stu-id="47af5-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="47af5-114">OS</span><span class="sxs-lookup"><span data-stu-id="47af5-114">PARAMETERS</span></span>

### <span data-ttu-id="47af5-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="47af5-115">-CacheId</span></span>
<span data-ttu-id="47af5-116">Identificador de um cache.</span><span class="sxs-lookup"><span data-stu-id="47af5-116">Identifier of a cache.</span></span>
<span data-ttu-id="47af5-117">Se especificado, você tentará localizar o cache pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="47af5-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="47af5-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="47af5-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47af5-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="47af5-119">-Context</span></span>
<span data-ttu-id="47af5-120">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="47af5-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="47af5-121">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="47af5-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47af5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47af5-122">-DefaultProfile</span></span>
<span data-ttu-id="47af5-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47af5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47af5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47af5-124">-ResourceId</span></span>
<span data-ttu-id="47af5-125">Identificador de recursos ARM de um cache.</span><span class="sxs-lookup"><span data-stu-id="47af5-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="47af5-126">Se especificado, você tentará localizar o cache pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="47af5-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="47af5-127">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="47af5-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47af5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47af5-128">CommonParameters</span></span>
<span data-ttu-id="47af5-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47af5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47af5-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47af5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47af5-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47af5-131">INPUTS</span></span>

### <span data-ttu-id="47af5-132">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="47af5-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47af5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="47af5-133">System.String</span></span>

## <span data-ttu-id="47af5-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47af5-134">OUTPUTS</span></span>

### <span data-ttu-id="47af5-135">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="47af5-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="47af5-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47af5-136">NOTES</span></span>

## <span data-ttu-id="47af5-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47af5-137">RELATED LINKS</span></span>

[<span data-ttu-id="47af5-138">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="47af5-138">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="47af5-139">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="47af5-139">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="47af5-140">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="47af5-140">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
