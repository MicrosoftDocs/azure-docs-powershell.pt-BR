---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 833351c3abbf95eb898405f23241a20fe9affefa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432673"
---
# <span data-ttu-id="d18b7-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="d18b7-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="d18b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d18b7-102">SYNOPSIS</span></span>
<span data-ttu-id="d18b7-103">Cria uma nova revisão de uma API existente.</span><span class="sxs-lookup"><span data-stu-id="d18b7-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="d18b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d18b7-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d18b7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d18b7-105">DESCRIPTION</span></span>

<span data-ttu-id="d18b7-106">O cmdlet **New-AzApiManagementApiRevision** cria uma revisão de API para uma API existente no contexto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="d18b7-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="d18b7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d18b7-107">EXAMPLES</span></span>

### <span data-ttu-id="d18b7-108">Exemplo 1: criar uma revisão de API vazia para uma API</span><span class="sxs-lookup"><span data-stu-id="d18b7-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="d18b7-109">Esse comando cria uma revisão `2` de API da `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="d18b7-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="d18b7-110">Exemplo 2: criar uma revisão de API a partir de uma API existente e copiar todas as operações, marcas e políticas</span><span class="sxs-lookup"><span data-stu-id="d18b7-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
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

<span data-ttu-id="d18b7-111">Esse comando cria uma revisão `5` de API da `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="d18b7-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="d18b7-112">OS</span><span class="sxs-lookup"><span data-stu-id="d18b7-112">PARAMETERS</span></span>

### <span data-ttu-id="d18b7-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d18b7-113">-ApiId</span></span>
<span data-ttu-id="d18b7-114">Identificador de API cuja revisão será criada.</span><span class="sxs-lookup"><span data-stu-id="d18b7-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="d18b7-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d18b7-115">-ApiRevision</span></span>
<span data-ttu-id="d18b7-116">Identificador de revisão da API.</span><span class="sxs-lookup"><span data-stu-id="d18b7-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="d18b7-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="d18b7-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="d18b7-118">Descrição da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="d18b7-118">Api Revision Description.</span></span> <span data-ttu-id="d18b7-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d18b7-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="d18b7-120">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d18b7-120">-Context</span></span>
<span data-ttu-id="d18b7-121">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d18b7-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d18b7-122">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="d18b7-122">This parameter is required.</span></span>

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

### <span data-ttu-id="d18b7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d18b7-123">-DefaultProfile</span></span>
<span data-ttu-id="d18b7-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d18b7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d18b7-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="d18b7-125">-ServiceUrl</span></span>
<span data-ttu-id="d18b7-126">Uma URL do serviço Web que expõe a API no serviço back-end.</span><span class="sxs-lookup"><span data-stu-id="d18b7-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="d18b7-127">Essa URL será usada apenas pelo gerenciamento de APIs do Azure e não será publicada.</span><span class="sxs-lookup"><span data-stu-id="d18b7-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="d18b7-128">Deve ter de 1 a 2000 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="d18b7-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="d18b7-129">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="d18b7-129">This parameter is required.</span></span>

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

### <span data-ttu-id="d18b7-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="d18b7-130">-SourceApiRevision</span></span>
<span data-ttu-id="d18b7-131">Identificador de revisão de API da API de origem.</span><span class="sxs-lookup"><span data-stu-id="d18b7-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="d18b7-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d18b7-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="d18b7-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d18b7-133">-Confirm</span></span>
<span data-ttu-id="d18b7-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d18b7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d18b7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d18b7-135">-WhatIf</span></span>
<span data-ttu-id="d18b7-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d18b7-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d18b7-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d18b7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d18b7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18b7-138">CommonParameters</span></span>
<span data-ttu-id="d18b7-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d18b7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18b7-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d18b7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18b7-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d18b7-141">INPUTS</span></span>

### <span data-ttu-id="d18b7-142">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d18b7-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d18b7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d18b7-143">System.String</span></span>

## <span data-ttu-id="d18b7-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d18b7-144">OUTPUTS</span></span>

### <span data-ttu-id="d18b7-145">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d18b7-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="d18b7-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d18b7-146">NOTES</span></span>

## <span data-ttu-id="d18b7-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d18b7-147">RELATED LINKS</span></span>

[<span data-ttu-id="d18b7-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d18b7-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="d18b7-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d18b7-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="d18b7-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d18b7-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
