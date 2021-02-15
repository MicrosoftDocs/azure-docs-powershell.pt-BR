---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 5a9141cf0f609eedd35c25f6fd3d7977201e58c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114842"
---
# <span data-ttu-id="f53e6-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f53e6-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="f53e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f53e6-102">SYNOPSIS</span></span>
<span data-ttu-id="f53e6-103">Importa uma API de um arquivo ou uma URL.</span><span class="sxs-lookup"><span data-stu-id="f53e6-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="f53e6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f53e6-104">SYNTAX</span></span>

### <span data-ttu-id="f53e6-105">ImportarFromLocalFile (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f53e6-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f53e6-106">ImportarFromUrl</span><span class="sxs-lookup"><span data-stu-id="f53e6-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f53e6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f53e6-107">DESCRIPTION</span></span>
<span data-ttu-id="f53e6-108">O cmdlet **Import-AzApiManagementApi** importa uma API de gerenciamento de API do Azure de um arquivo ou uma URL no formato DESCRIÇÃO do Aplicativo Web (URL), WSDL (Linguagem de Descrição dos Serviços Web) ou formato Desmancha.</span><span class="sxs-lookup"><span data-stu-id="f53e6-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="f53e6-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f53e6-109">EXAMPLES</span></span>

### <span data-ttu-id="f53e6-110">Exemplo 1: Importar uma API de um arquivo WADEL</span><span class="sxs-lookup"><span data-stu-id="f53e6-110">Example 1: Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="f53e6-111">Esse comando importa uma API do arquivo COTAL especificado.</span><span class="sxs-lookup"><span data-stu-id="f53e6-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="f53e6-112">Exemplo 2: Importar uma API de um arquivo Descarada</span><span class="sxs-lookup"><span data-stu-id="f53e6-112">Example 2: Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="f53e6-113">Esse comando importa uma API do arquivo Descarado especificado.</span><span class="sxs-lookup"><span data-stu-id="f53e6-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="f53e6-114">Exemplo 3: Importar uma API de um link DESL</span><span class="sxs-lookup"><span data-stu-id="f53e6-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="f53e6-115">Esse comando importa uma API do link DESL especificado.</span><span class="sxs-lookup"><span data-stu-id="f53e6-115">This command imports an API from the specified WADL link.</span></span>

### <span data-ttu-id="f53e6-116">Exemplo 4: Importar uma API de um Link open api</span><span class="sxs-lookup"><span data-stu-id="f53e6-116">Example 4: Import an API from a Open Api Link</span></span>
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

<span data-ttu-id="f53e6-117">Esse comando importa uma API do link de especificação Open 3.0 especificado.</span><span class="sxs-lookup"><span data-stu-id="f53e6-117">This command imports an API from the specified Open 3.0 specification link.</span></span>

### <span data-ttu-id="f53e6-118">Exemplo 5: Importar uma API de um Link da Api Open para um Conjunto de ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f53e6-118">Example 5:  Import an API from a Open Api Link into a ApiVersion Set</span></span>

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

<span data-ttu-id="f53e6-119">Esse comando importa uma API do documento de especificação Open 3.0 especificado e cria um novo ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="f53e6-119">This command imports an API from the specified Open 3.0 specification document and create a new ApiVersion.</span></span>

## <span data-ttu-id="f53e6-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f53e6-120">PARAMETERS</span></span>

### <span data-ttu-id="f53e6-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f53e6-121">-ApiId</span></span>
<span data-ttu-id="f53e6-122">Especifica uma ID da API a ser importada.</span><span class="sxs-lookup"><span data-stu-id="f53e6-122">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="f53e6-123">Se você não especificar esse parâmetro, uma ID será gerada para você.</span><span class="sxs-lookup"><span data-stu-id="f53e6-123">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="f53e6-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f53e6-124">-ApiRevision</span></span>
<span data-ttu-id="f53e6-125">Identificador de Revisão da API.</span><span class="sxs-lookup"><span data-stu-id="f53e6-125">Identifier of API Revision.</span></span> <span data-ttu-id="f53e6-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f53e6-126">This parameter is optional.</span></span> <span data-ttu-id="f53e6-127">Se não especificado, a importação será feita na revisão ativa no momento ou em uma nova api.</span><span class="sxs-lookup"><span data-stu-id="f53e6-127">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="f53e6-128">-ApiType</span><span class="sxs-lookup"><span data-stu-id="f53e6-128">-ApiType</span></span>
<span data-ttu-id="f53e6-129">Este parâmetro é opcional com um valor padrão de Http.</span><span class="sxs-lookup"><span data-stu-id="f53e6-129">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="f53e6-130">A opção Soap só é aplicável ao importar o WSDL e criará uma API SOAP Passthrough.</span><span class="sxs-lookup"><span data-stu-id="f53e6-130">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="f53e6-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f53e6-131">-ApiVersion</span></span>
<span data-ttu-id="f53e6-132">Api Version of the Api to create.</span><span class="sxs-lookup"><span data-stu-id="f53e6-132">Api Version of the Api to create.</span></span> <span data-ttu-id="f53e6-133">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f53e6-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="f53e6-134">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="f53e6-134">-ApiVersionSetId</span></span>
<span data-ttu-id="f53e6-135">Um identificador de recurso para o Conjunto de Versão da Api relacionado.</span><span class="sxs-lookup"><span data-stu-id="f53e6-135">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="f53e6-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f53e6-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="f53e6-137">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f53e6-137">-Context</span></span>
<span data-ttu-id="f53e6-138">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="f53e6-138">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f53e6-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f53e6-139">-DefaultProfile</span></span>
<span data-ttu-id="f53e6-140">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f53e6-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f53e6-141">-Caminho</span><span class="sxs-lookup"><span data-stu-id="f53e6-141">-Path</span></span>
<span data-ttu-id="f53e6-142">Especifica um caminho de API da Web como a última parte da URL pública da API.</span><span class="sxs-lookup"><span data-stu-id="f53e6-142">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="f53e6-143">Essa URL é usada pelos consumidores da API para enviar solicitações para o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="f53e6-143">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="f53e6-144">Deve ter de 1 a 400 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f53e6-144">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="f53e6-145">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="f53e6-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="f53e6-146">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="f53e6-146">-Protocol</span></span>
<span data-ttu-id="f53e6-147">Protocolos de API da Web (https).</span><span class="sxs-lookup"><span data-stu-id="f53e6-147">Web API protocols (http, https).</span></span> <span data-ttu-id="f53e6-148">Protocolos sobre os quais a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="f53e6-148">Protocols over which API is made available.</span></span> <span data-ttu-id="f53e6-149">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f53e6-149">This parameter is optional.</span></span> <span data-ttu-id="f53e6-150">Se fornecido, ele substituirá os protocolos especificados no documento de especificações.</span><span class="sxs-lookup"><span data-stu-id="f53e6-150">If provided it will override the protocols specified in the specifications document.</span></span>

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

### <span data-ttu-id="f53e6-151">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="f53e6-151">-ServiceUrl</span></span>
<span data-ttu-id="f53e6-152">Uma URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="f53e6-152">A URL of the web service exposing the API.</span></span> <span data-ttu-id="f53e6-153">Essa URL será usada apenas pelo Gerenciamento de API do Azure e não será pública.</span><span class="sxs-lookup"><span data-stu-id="f53e6-153">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="f53e6-154">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f53e6-154">This parameter is optional.</span></span> <span data-ttu-id="f53e6-155">Se fornecido, ele substituirá a ServiceUrl especificada no documento Especificações.</span><span class="sxs-lookup"><span data-stu-id="f53e6-155">If provided it will override the ServiceUrl specified in the Specifications document.</span></span>

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

### <span data-ttu-id="f53e6-156">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="f53e6-156">-SpecificationFormat</span></span>
<span data-ttu-id="f53e6-157">Especifica o formato de especificação.</span><span class="sxs-lookup"><span data-stu-id="f53e6-157">Specifies the specification format.</span></span>
<span data-ttu-id="f53e6-158">psdx_paramvalues, Badal, Wsdl e Seta.</span><span class="sxs-lookup"><span data-stu-id="f53e6-158">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

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

### <span data-ttu-id="f53e6-159">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="f53e6-159">-SpecificationPath</span></span>
<span data-ttu-id="f53e6-160">Especifica o caminho do arquivo de especificação.</span><span class="sxs-lookup"><span data-stu-id="f53e6-160">Specifies the specification file path.</span></span>

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

### <span data-ttu-id="f53e6-161">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="f53e6-161">-SpecificationUrl</span></span>
<span data-ttu-id="f53e6-162">Especifica a URL da especificação.</span><span class="sxs-lookup"><span data-stu-id="f53e6-162">Specifies the specification URL.</span></span>

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

### <span data-ttu-id="f53e6-163">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="f53e6-163">-WsdlEndpointName</span></span>
<span data-ttu-id="f53e6-164">Nome local do Ponto de Extremidade WSDL (porta) a ser importado.</span><span class="sxs-lookup"><span data-stu-id="f53e6-164">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="f53e6-165">Deve ter de 1 a 400 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f53e6-165">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="f53e6-166">Este parâmetro é opcional e só é necessário para importar wsdl.</span><span class="sxs-lookup"><span data-stu-id="f53e6-166">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="f53e6-167">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="f53e6-167">Default value is $null.</span></span>

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

### <span data-ttu-id="f53e6-168">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="f53e6-168">-WsdlServiceName</span></span>
<span data-ttu-id="f53e6-169">Nome local do Serviço WSDL a ser importado.</span><span class="sxs-lookup"><span data-stu-id="f53e6-169">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="f53e6-170">Deve ter de 1 a 400 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f53e6-170">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="f53e6-171">Este parâmetro é opcional e só é necessário para importar wsdl.</span><span class="sxs-lookup"><span data-stu-id="f53e6-171">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="f53e6-172">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="f53e6-172">Default value is $null.</span></span>

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

### <span data-ttu-id="f53e6-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f53e6-173">CommonParameters</span></span>
<span data-ttu-id="f53e6-174">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f53e6-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f53e6-175">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f53e6-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f53e6-176">Entradas</span><span class="sxs-lookup"><span data-stu-id="f53e6-176">INPUTS</span></span>

### <span data-ttu-id="f53e6-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f53e6-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f53e6-178">System.String</span><span class="sxs-lookup"><span data-stu-id="f53e6-178">System.String</span></span>

### <span data-ttu-id="f53e6-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="f53e6-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="f53e6-180">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f53e6-180">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f53e6-181">Saídas</span><span class="sxs-lookup"><span data-stu-id="f53e6-181">OUTPUTS</span></span>

### <span data-ttu-id="f53e6-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f53e6-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="f53e6-183">Notas</span><span class="sxs-lookup"><span data-stu-id="f53e6-183">NOTES</span></span>

## <span data-ttu-id="f53e6-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f53e6-184">RELATED LINKS</span></span>

[<span data-ttu-id="f53e6-185">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f53e6-185">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="f53e6-186">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f53e6-186">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="f53e6-187">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f53e6-187">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="f53e6-188">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f53e6-188">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="f53e6-189">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f53e6-189">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


