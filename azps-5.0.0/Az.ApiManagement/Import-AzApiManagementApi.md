---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 5a9141cf0f609eedd35c25f6fd3d7977201e58c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116462"
---
# <span data-ttu-id="de969-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="de969-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="de969-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de969-102">SYNOPSIS</span></span>
<span data-ttu-id="de969-103">Importa uma API de um arquivo ou de uma URL.</span><span class="sxs-lookup"><span data-stu-id="de969-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="de969-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de969-104">SYNTAX</span></span>

### <span data-ttu-id="de969-105">ImportFromLocalFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="de969-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de969-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="de969-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de969-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de969-107">DESCRIPTION</span></span>
<span data-ttu-id="de969-108">O cmdlet **Import-AzApiManagementApi** importa uma API de gerenciamento de API do Azure de um arquivo ou uma URL na linguagem de descrição de aplicativo Web (WADL), Web Services Description Language (WSDL) ou no formato Swagger.</span><span class="sxs-lookup"><span data-stu-id="de969-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="de969-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de969-109">EXAMPLES</span></span>

### <span data-ttu-id="de969-110">Exemplo 1: importar uma API de um arquivo WADL</span><span class="sxs-lookup"><span data-stu-id="de969-110">Example 1: Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="de969-111">Esse comando importa uma API do arquivo WADL especificado.</span><span class="sxs-lookup"><span data-stu-id="de969-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="de969-112">Exemplo 2: importar uma API de um arquivo Swagger</span><span class="sxs-lookup"><span data-stu-id="de969-112">Example 2: Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="de969-113">Esse comando importa uma API do arquivo Swagger especificado.</span><span class="sxs-lookup"><span data-stu-id="de969-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="de969-114">Exemplo 3: importar uma API de um link WADL</span><span class="sxs-lookup"><span data-stu-id="de969-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="de969-115">Esse comando importa uma API do link WADL especificado.</span><span class="sxs-lookup"><span data-stu-id="de969-115">This command imports an API from the specified WADL link.</span></span>

### <span data-ttu-id="de969-116">Exemplo 4: importar uma API de um link de API aberta</span><span class="sxs-lookup"><span data-stu-id="de969-116">Example 4: Import an API from a Open Api Link</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationFormat OpenApi -SpecificationUrl https://raw.githubusercontent.com/OAI/OpenAPI-Specification/master/examples/v3.0/petstore.yaml -Path "petstore30"

ApiId                         : af3f57bab399455aa875d7050654e9d1
Name                          : Swagger Petstore
Description                   :
ServiceUrl                    : http://petstore.swagger.io/v1
Path                          : petstore30
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    :
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/af3f57bab399455aa875d7050654e9d1     
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="de969-117">Esse comando importa uma API do link de especificação Open 3,0 especificado.</span><span class="sxs-lookup"><span data-stu-id="de969-117">This command imports an API from the specified Open 3.0 specification link.</span></span>

### <span data-ttu-id="de969-118">Exemplo 5: importar uma API de um link de API aberta para um conjunto de ApiVersion</span><span class="sxs-lookup"><span data-stu-id="de969-118">Example 5:  Import an API from a Open Api Link into a ApiVersion Set</span></span>

```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationPath "C:\contoso\specifications\uspto.yml" -SpecificationFormat OpenApi -Path uspostal -ApiVersionSetId 0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd -ApiVersion v2

ApiId                         : 6c3f20c66e5745b19229d06cd865948f
Name                          : USPTO Data Set API
Description                   : The Data Set API (DSAPI) allows the public users to discover and search USPTO exported data sets. This is a generic API that allows USPTO users to make any CSV based data files
                                searchable through API. With the help of GET call, it returns the list of data fields that are searchable. With the help of POST call, data can be fetched based on the filters on the    
                                field names. Please note that POST call is used to search the actual data. The reason for the POST call is that it allows users to specify any complex search criteria without worry      
                                about the GET size limitations as well as encoding of the input parameters.
ServiceUrl                    : https://developer.uspto.gov/ds-api
Path                          : uspostal
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v2
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd
Id                            : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis/6c3f20c66e5745b19229d06cd865948f    
ResourceGroupName             : Api-Default-East-US
ServiceName                   : contoso
```

<span data-ttu-id="de969-119">Esse comando importa uma API do documento de especificação Open 3,0 especificado e cria um novo ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="de969-119">This command imports an API from the specified Open 3.0 specification document and create a new ApiVersion.</span></span>

## <span data-ttu-id="de969-120">OS</span><span class="sxs-lookup"><span data-stu-id="de969-120">PARAMETERS</span></span>

### <span data-ttu-id="de969-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="de969-121">-ApiId</span></span>
<span data-ttu-id="de969-122">Especifica uma ID para a API a ser importada.</span><span class="sxs-lookup"><span data-stu-id="de969-122">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="de969-123">Se você não especificar esse parâmetro, uma ID será gerada para você.</span><span class="sxs-lookup"><span data-stu-id="de969-123">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="de969-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="de969-124">-ApiRevision</span></span>
<span data-ttu-id="de969-125">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="de969-125">Identifier of API Revision.</span></span> <span data-ttu-id="de969-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="de969-126">This parameter is optional.</span></span> <span data-ttu-id="de969-127">Se não for especificado, a importação será feita na revisão ativa no momento ou em uma nova API.</span><span class="sxs-lookup"><span data-stu-id="de969-127">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="de969-128">-ApiType</span><span class="sxs-lookup"><span data-stu-id="de969-128">-ApiType</span></span>
<span data-ttu-id="de969-129">Esse parâmetro é opcional com um valor padrão de http.</span><span class="sxs-lookup"><span data-stu-id="de969-129">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="de969-130">A opção SOAP só se aplica ao importar WSDL e criar uma API de passagem SOAP.</span><span class="sxs-lookup"><span data-stu-id="de969-130">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de969-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="de969-131">-ApiVersion</span></span>
<span data-ttu-id="de969-132">Versão de API da API a ser criada.</span><span class="sxs-lookup"><span data-stu-id="de969-132">Api Version of the Api to create.</span></span> <span data-ttu-id="de969-133">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="de969-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="de969-134">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="de969-134">-ApiVersionSetId</span></span>
<span data-ttu-id="de969-135">Um identificador de recurso para o conjunto de versões de API relacionado.</span><span class="sxs-lookup"><span data-stu-id="de969-135">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="de969-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="de969-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="de969-137">-Contexto</span><span class="sxs-lookup"><span data-stu-id="de969-137">-Context</span></span>
<span data-ttu-id="de969-138">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="de969-138">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de969-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de969-139">-DefaultProfile</span></span>
<span data-ttu-id="de969-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de969-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de969-141">-Caminho</span><span class="sxs-lookup"><span data-stu-id="de969-141">-Path</span></span>
<span data-ttu-id="de969-142">Especifica um caminho de API Web como a última parte da URL pública da API.</span><span class="sxs-lookup"><span data-stu-id="de969-142">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="de969-143">Essa URL é usada por consumidores de API para enviar solicitações ao serviço Web.</span><span class="sxs-lookup"><span data-stu-id="de969-143">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="de969-144">Deve ter de 1 a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="de969-144">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="de969-145">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="de969-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="de969-146">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="de969-146">-Protocol</span></span>
<span data-ttu-id="de969-147">Protocolos de API Web (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="de969-147">Web API protocols (http, https).</span></span> <span data-ttu-id="de969-148">Protocolos em que a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="de969-148">Protocols over which API is made available.</span></span> <span data-ttu-id="de969-149">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="de969-149">This parameter is optional.</span></span> <span data-ttu-id="de969-150">Se fornecido, ele substituirá os protocolos especificados no documento especificações.</span><span class="sxs-lookup"><span data-stu-id="de969-150">If provided it will override the protocols specified in the specifications document.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de969-151">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="de969-151">-ServiceUrl</span></span>
<span data-ttu-id="de969-152">Uma URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="de969-152">A URL of the web service exposing the API.</span></span> <span data-ttu-id="de969-153">Essa URL será usada apenas pelo gerenciamento de APIs do Azure e não será publicada.</span><span class="sxs-lookup"><span data-stu-id="de969-153">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="de969-154">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="de969-154">This parameter is optional.</span></span> <span data-ttu-id="de969-155">Se o fornecido, ele substituirá o ServiceUrl especificado no documento de especificações.</span><span class="sxs-lookup"><span data-stu-id="de969-155">If provided it will override the ServiceUrl specified in the Specifications document.</span></span>

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

### <span data-ttu-id="de969-156">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="de969-156">-SpecificationFormat</span></span>
<span data-ttu-id="de969-157">Especifica o formato de especificação.</span><span class="sxs-lookup"><span data-stu-id="de969-157">Specifies the specification format.</span></span>
<span data-ttu-id="de969-158">psdx_paramvalues WADL, WSDL e Swagger.</span><span class="sxs-lookup"><span data-stu-id="de969-158">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de969-159">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="de969-159">-SpecificationPath</span></span>
<span data-ttu-id="de969-160">Especifica o caminho do arquivo de especificação.</span><span class="sxs-lookup"><span data-stu-id="de969-160">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromLocalFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de969-161">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="de969-161">-SpecificationUrl</span></span>
<span data-ttu-id="de969-162">Especifica a URL de especificação.</span><span class="sxs-lookup"><span data-stu-id="de969-162">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de969-163">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="de969-163">-WsdlEndpointName</span></span>
<span data-ttu-id="de969-164">Nome local do ponto de extremidade (porta) WSDL a ser importado.</span><span class="sxs-lookup"><span data-stu-id="de969-164">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="de969-165">Deve ter de 1 a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="de969-165">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="de969-166">Esse parâmetro é opcional e só é necessário para importar WSDL.</span><span class="sxs-lookup"><span data-stu-id="de969-166">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="de969-167">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="de969-167">Default value is $null.</span></span>

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

### <span data-ttu-id="de969-168">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="de969-168">-WsdlServiceName</span></span>
<span data-ttu-id="de969-169">Nome local do serviço WSDL a ser importado.</span><span class="sxs-lookup"><span data-stu-id="de969-169">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="de969-170">Deve ter de 1 a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="de969-170">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="de969-171">Esse parâmetro é opcional e só é necessário para importar WSDL.</span><span class="sxs-lookup"><span data-stu-id="de969-171">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="de969-172">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="de969-172">Default value is $null.</span></span>

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

### <span data-ttu-id="de969-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de969-173">CommonParameters</span></span>
<span data-ttu-id="de969-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de969-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de969-175">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de969-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de969-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de969-176">INPUTS</span></span>

### <span data-ttu-id="de969-177">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="de969-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="de969-178">System. String</span><span class="sxs-lookup"><span data-stu-id="de969-178">System.String</span></span>

### <span data-ttu-id="de969-179">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="de969-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="de969-180">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Management. Models. PsApiManagementApiType, Microsoft. Azure. PowerShell. cmdlets. ApiManagement. immanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="de969-180">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="de969-181">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de969-181">OUTPUTS</span></span>

### <span data-ttu-id="de969-182">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="de969-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="de969-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de969-183">NOTES</span></span>

## <span data-ttu-id="de969-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de969-184">RELATED LINKS</span></span>

[<span data-ttu-id="de969-185">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="de969-185">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="de969-186">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="de969-186">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="de969-187">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="de969-187">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="de969-188">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="de969-188">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="de969-189">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="de969-189">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


