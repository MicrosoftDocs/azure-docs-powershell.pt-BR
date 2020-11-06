---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 690ebbfb1bb3cca6de8feb1f199068510e41f1d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595658"
---
# <span data-ttu-id="79454-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79454-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="79454-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79454-102">SYNOPSIS</span></span>
<span data-ttu-id="79454-103">Importa uma API de um arquivo ou de uma URL.</span><span class="sxs-lookup"><span data-stu-id="79454-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="79454-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79454-104">SYNTAX</span></span>

### <span data-ttu-id="79454-105">ImportFromLocalFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="79454-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79454-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="79454-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79454-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79454-107">DESCRIPTION</span></span>
<span data-ttu-id="79454-108">O cmdlet **Import-AzApiManagementApi** importa uma API de gerenciamento de API do Azure de um arquivo ou uma URL na linguagem de descrição de aplicativo Web (WADL), Web Services Description Language (WSDL) ou no formato Swagger.</span><span class="sxs-lookup"><span data-stu-id="79454-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="79454-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79454-109">EXAMPLES</span></span>

### <span data-ttu-id="79454-110">Exemplo 1 importar uma API de um arquivo WADL</span><span class="sxs-lookup"><span data-stu-id="79454-110">Example 1 Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="79454-111">Esse comando importa uma API do arquivo WADL especificado.</span><span class="sxs-lookup"><span data-stu-id="79454-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="79454-112">Exemplo 2 importar uma API de um arquivo Swagger</span><span class="sxs-lookup"><span data-stu-id="79454-112">Example 2 Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="79454-113">Esse comando importa uma API do arquivo Swagger especificado.</span><span class="sxs-lookup"><span data-stu-id="79454-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="79454-114">Exemplo 3: importar uma API de um link WADL</span><span class="sxs-lookup"><span data-stu-id="79454-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="79454-115">Esse comando importa uma API do link WADL especificado.</span><span class="sxs-lookup"><span data-stu-id="79454-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="79454-116">OS</span><span class="sxs-lookup"><span data-stu-id="79454-116">PARAMETERS</span></span>

### <span data-ttu-id="79454-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="79454-117">-ApiId</span></span>
<span data-ttu-id="79454-118">Especifica uma ID para a API a ser importada.</span><span class="sxs-lookup"><span data-stu-id="79454-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="79454-119">Se você não especificar esse parâmetro, uma ID será gerada para você.</span><span class="sxs-lookup"><span data-stu-id="79454-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="79454-120">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="79454-120">-ApiRevision</span></span>
<span data-ttu-id="79454-121">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="79454-121">Identifier of API Revision.</span></span> <span data-ttu-id="79454-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="79454-122">This parameter is optional.</span></span> <span data-ttu-id="79454-123">Se não for especificado, a importação será feita na revisão ativa no momento ou em uma nova API.</span><span class="sxs-lookup"><span data-stu-id="79454-123">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="79454-124">-ApiType</span><span class="sxs-lookup"><span data-stu-id="79454-124">-ApiType</span></span>
<span data-ttu-id="79454-125">Esse parâmetro é opcional com um valor padrão de http.</span><span class="sxs-lookup"><span data-stu-id="79454-125">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="79454-126">A opção SOAP só se aplica ao importar WSDL e criar uma API de passagem SOAP.</span><span class="sxs-lookup"><span data-stu-id="79454-126">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="79454-127">-Contexto</span><span class="sxs-lookup"><span data-stu-id="79454-127">-Context</span></span>
<span data-ttu-id="79454-128">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="79454-128">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79454-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79454-129">-DefaultProfile</span></span>
<span data-ttu-id="79454-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79454-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79454-131">-Caminho</span><span class="sxs-lookup"><span data-stu-id="79454-131">-Path</span></span>
<span data-ttu-id="79454-132">Especifica um caminho de API Web como a última parte da URL pública da API.</span><span class="sxs-lookup"><span data-stu-id="79454-132">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="79454-133">Essa URL é usada por consumidores de API para enviar solicitações ao serviço Web.</span><span class="sxs-lookup"><span data-stu-id="79454-133">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="79454-134">Deve ter de 1 a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="79454-134">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="79454-135">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="79454-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="79454-136">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="79454-136">-SpecificationFormat</span></span>
<span data-ttu-id="79454-137">Especifica o formato de especificação.</span><span class="sxs-lookup"><span data-stu-id="79454-137">Specifies the specification format.</span></span>
<span data-ttu-id="79454-138">psdx_paramvalues WADL, WSDL e Swagger.</span><span class="sxs-lookup"><span data-stu-id="79454-138">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79454-139">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="79454-139">-SpecificationPath</span></span>
<span data-ttu-id="79454-140">Especifica o caminho do arquivo de especificação.</span><span class="sxs-lookup"><span data-stu-id="79454-140">Specifies the specification file path.</span></span>

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

### <span data-ttu-id="79454-141">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="79454-141">-SpecificationUrl</span></span>
<span data-ttu-id="79454-142">Especifica a URL de especificação.</span><span class="sxs-lookup"><span data-stu-id="79454-142">Specifies the specification URL.</span></span>

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

### <span data-ttu-id="79454-143">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="79454-143">-WsdlEndpointName</span></span>
<span data-ttu-id="79454-144">Nome local do ponto de extremidade (porta) WSDL a ser importado.</span><span class="sxs-lookup"><span data-stu-id="79454-144">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="79454-145">Deve ter de 1 a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="79454-145">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="79454-146">Esse parâmetro é opcional e só é necessário para importar WSDL.</span><span class="sxs-lookup"><span data-stu-id="79454-146">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="79454-147">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="79454-147">Default value is $null.</span></span>

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

### <span data-ttu-id="79454-148">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="79454-148">-WsdlServiceName</span></span>
<span data-ttu-id="79454-149">Nome local do serviço WSDL a ser importado.</span><span class="sxs-lookup"><span data-stu-id="79454-149">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="79454-150">Deve ter de 1 a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="79454-150">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="79454-151">Esse parâmetro é opcional e só é necessário para importar WSDL.</span><span class="sxs-lookup"><span data-stu-id="79454-151">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="79454-152">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="79454-152">Default value is $null.</span></span>

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

### <span data-ttu-id="79454-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79454-153">CommonParameters</span></span>
<span data-ttu-id="79454-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79454-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79454-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79454-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79454-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79454-156">INPUTS</span></span>

### <span data-ttu-id="79454-157">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="79454-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="79454-158">System. String</span><span class="sxs-lookup"><span data-stu-id="79454-158">System.String</span></span>

### <span data-ttu-id="79454-159">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="79454-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="79454-160">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Management. Models. PsApiManagementApiType, Microsoft. Azure. PowerShell. cmdlets. ApiManagement. immanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="79454-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="79454-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79454-161">OUTPUTS</span></span>

### <span data-ttu-id="79454-162">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79454-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="79454-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79454-163">NOTES</span></span>

## <span data-ttu-id="79454-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79454-164">RELATED LINKS</span></span>

[<span data-ttu-id="79454-165">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79454-165">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="79454-166">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79454-166">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="79454-167">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79454-167">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="79454-168">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79454-168">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="79454-169">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79454-169">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


