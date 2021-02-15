---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: fee978a1500c0fc472ec8015a3e8dbbbdc8015bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118085"
---
# <span data-ttu-id="bedb3-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="bedb3-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="bedb3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bedb3-102">SYNOPSIS</span></span>
<span data-ttu-id="bedb3-103">Obter os detalhes do Cache.</span><span class="sxs-lookup"><span data-stu-id="bedb3-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="bedb3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bedb3-104">SYNTAX</span></span>

### <span data-ttu-id="bedb3-105">ContextParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bedb3-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bedb3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bedb3-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bedb3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bedb3-107">DESCRIPTION</span></span>
<span data-ttu-id="bedb3-108">Obter os detalhes do Cache configurado no serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="bedb3-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="bedb3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bedb3-109">EXAMPLES</span></span>

### <span data-ttu-id="bedb3-110">Exemplo 1: Obter todos os Caches</span><span class="sxs-lookup"><span data-stu-id="bedb3-110">Example 1: Get all Caches</span></span>
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

<span data-ttu-id="bedb3-111">Obtém uma lista de todos os Caches configurados no serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="bedb3-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="bedb3-112">Exemplo 2: Obter o Cache especificado pelo identificador westus</span><span class="sxs-lookup"><span data-stu-id="bedb3-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
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

<span data-ttu-id="bedb3-113">Obter os detalhes do Cache especificado configurado para westus</span><span class="sxs-lookup"><span data-stu-id="bedb3-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="bedb3-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bedb3-114">PARAMETERS</span></span>

### <span data-ttu-id="bedb3-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="bedb3-115">-CacheId</span></span>
<span data-ttu-id="bedb3-116">Identificador de um cache.</span><span class="sxs-lookup"><span data-stu-id="bedb3-116">Identifier of a cache.</span></span>
<span data-ttu-id="bedb3-117">Se especificado, tentará encontrar o cache pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="bedb3-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="bedb3-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="bedb3-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="bedb3-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="bedb3-119">-Context</span></span>
<span data-ttu-id="bedb3-120">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bedb3-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bedb3-121">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="bedb3-121">This parameter is required.</span></span>

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

### <span data-ttu-id="bedb3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bedb3-122">-DefaultProfile</span></span>
<span data-ttu-id="bedb3-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bedb3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bedb3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bedb3-124">-ResourceId</span></span>
<span data-ttu-id="bedb3-125">Arm Resource Identifier de um cache.</span><span class="sxs-lookup"><span data-stu-id="bedb3-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="bedb3-126">Se especificado, tentará encontrar o cache pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="bedb3-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="bedb3-127">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="bedb3-127">This parameter is required.</span></span>

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

### <span data-ttu-id="bedb3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bedb3-128">CommonParameters</span></span>
<span data-ttu-id="bedb3-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bedb3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bedb3-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bedb3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bedb3-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="bedb3-131">INPUTS</span></span>

### <span data-ttu-id="bedb3-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bedb3-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bedb3-133">System.String</span><span class="sxs-lookup"><span data-stu-id="bedb3-133">System.String</span></span>

## <span data-ttu-id="bedb3-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="bedb3-134">OUTPUTS</span></span>

### <span data-ttu-id="bedb3-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="bedb3-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="bedb3-136">Notas</span><span class="sxs-lookup"><span data-stu-id="bedb3-136">NOTES</span></span>

## <span data-ttu-id="bedb3-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bedb3-137">RELATED LINKS</span></span>

[<span data-ttu-id="bedb3-138">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="bedb3-138">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="bedb3-139">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="bedb3-139">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="bedb3-140">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="bedb3-140">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
