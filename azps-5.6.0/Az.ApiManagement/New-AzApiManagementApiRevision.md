---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: d03253a608469ac111d04b837497375028b48fe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892828"
---
# <span data-ttu-id="68cd2-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="68cd2-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="68cd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="68cd2-103">Cria uma nova Revisão de uma API existente.</span><span class="sxs-lookup"><span data-stu-id="68cd2-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="68cd2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="68cd2-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68cd2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="68cd2-105">DESCRIPTION</span></span>

<span data-ttu-id="68cd2-106">O cmdlet **New-AzApiManagementApiRevision** cria uma Revisão de API para uma API existente no contexto de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="68cd2-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="68cd2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68cd2-107">EXAMPLES</span></span>

### <span data-ttu-id="68cd2-108">Exemplo 1: Criar uma revisão de API vazia para uma API</span><span class="sxs-lookup"><span data-stu-id="68cd2-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="68cd2-109">Este comando cria uma Revisão de API `2` da `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="68cd2-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="68cd2-110">Exemplo 2: Criar uma Revisão de API a partir de uma Api Existente e copiar Todas as operações, marcas e políticas</span><span class="sxs-lookup"><span data-stu-id="68cd2-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5" -SourceApiRevision "1" -ServiceUrl "https://echoapi.cloudapp.net/rev4"


ApiId                         : echo-api;rev=5
Name                          : Echo API
Description                   :
ServiceUrl                    : http://echoapi.cloudapp.net/api
Path                          : echo
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 5
ApiVersion                    :
IsCurrent                     : False
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/apimService1/providers/Microsoft.ApiManagement/service/sdktestapim4163/apis/echo-api;rev=5
ResourceGroupName             : apimService1
ServiceName                   : sdktestapim4163
```

<span data-ttu-id="68cd2-111">Este comando cria uma Revisão de API `5` da `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="68cd2-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="68cd2-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="68cd2-112">PARAMETERS</span></span>

### <span data-ttu-id="68cd2-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="68cd2-113">-ApiId</span></span>
<span data-ttu-id="68cd2-114">Identificador da API cuja Revisão deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="68cd2-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="68cd2-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="68cd2-115">-ApiRevision</span></span>
<span data-ttu-id="68cd2-116">Identificador de revisão da Api.</span><span class="sxs-lookup"><span data-stu-id="68cd2-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="68cd2-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="68cd2-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="68cd2-118">Api Revision Description.</span><span class="sxs-lookup"><span data-stu-id="68cd2-118">Api Revision Description.</span></span> <span data-ttu-id="68cd2-119">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="68cd2-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="68cd2-120">-Context</span><span class="sxs-lookup"><span data-stu-id="68cd2-120">-Context</span></span>
<span data-ttu-id="68cd2-121">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="68cd2-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="68cd2-122">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="68cd2-122">This parameter is required.</span></span>

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

### <span data-ttu-id="68cd2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68cd2-123">-DefaultProfile</span></span>
<span data-ttu-id="68cd2-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68cd2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68cd2-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="68cd2-125">-ServiceUrl</span></span>
<span data-ttu-id="68cd2-126">Uma URL do serviço Web expondo a API no serviço Backend.</span><span class="sxs-lookup"><span data-stu-id="68cd2-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="68cd2-127">Essa URL será usada apenas pelo Gerenciamento de API do Azure e não será pública.</span><span class="sxs-lookup"><span data-stu-id="68cd2-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="68cd2-128">Deve ter de 1 a 2000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="68cd2-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="68cd2-129">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="68cd2-129">This parameter is required.</span></span>

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

### <span data-ttu-id="68cd2-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="68cd2-130">-SourceApiRevision</span></span>
<span data-ttu-id="68cd2-131">Identificador de Revisão de Api da API de origem.</span><span class="sxs-lookup"><span data-stu-id="68cd2-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="68cd2-132">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="68cd2-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="68cd2-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68cd2-133">-Confirm</span></span>
<span data-ttu-id="68cd2-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68cd2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68cd2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68cd2-135">-WhatIf</span></span>
<span data-ttu-id="68cd2-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="68cd2-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68cd2-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="68cd2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68cd2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68cd2-138">CommonParameters</span></span>
<span data-ttu-id="68cd2-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68cd2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68cd2-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68cd2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68cd2-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68cd2-141">INPUTS</span></span>

### <span data-ttu-id="68cd2-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="68cd2-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="68cd2-143">System.String</span><span class="sxs-lookup"><span data-stu-id="68cd2-143">System.String</span></span>

## <span data-ttu-id="68cd2-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="68cd2-144">OUTPUTS</span></span>

### <span data-ttu-id="68cd2-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="68cd2-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="68cd2-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="68cd2-146">NOTES</span></span>

## <span data-ttu-id="68cd2-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68cd2-147">RELATED LINKS</span></span>

[<span data-ttu-id="68cd2-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="68cd2-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="68cd2-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="68cd2-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="68cd2-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="68cd2-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
