---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: 5e00f3718b093f3112839ebb331fc96984a03038
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610439"
---
# <span data-ttu-id="72b40-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="72b40-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="72b40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72b40-102">SYNOPSIS</span></span>
<span data-ttu-id="72b40-103">Importa uma API de um arquivo ou de uma URL.</span><span class="sxs-lookup"><span data-stu-id="72b40-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72b40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72b40-104">SYNTAX</span></span>

### <span data-ttu-id="72b40-105">ImportFromLocalFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="72b40-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72b40-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="72b40-106">ImportFromUrl</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72b40-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72b40-107">DESCRIPTION</span></span>
<span data-ttu-id="72b40-108">O cmdlet **Import-AzureRmApiManagementApi** importa uma API de gerenciamento de API do Azure de um arquivo ou uma URL na linguagem de descrição de aplicativo Web (WADL), Web Services Description Language (WSDL) ou no formato Swagger.</span><span class="sxs-lookup"><span data-stu-id="72b40-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="72b40-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72b40-109">EXAMPLES</span></span>

### <span data-ttu-id="72b40-110">Exemplo 1 importar uma API de um arquivo WADL</span><span class="sxs-lookup"><span data-stu-id="72b40-110">Example 1 Import an API from a WADL file</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="72b40-111">Esse comando importa uma API do arquivo WADL especificado.</span><span class="sxs-lookup"><span data-stu-id="72b40-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="72b40-112">Exemplo 2 importar uma API de um arquivo Swagger</span><span class="sxs-lookup"><span data-stu-id="72b40-112">Example 2 Import an API from a Swagger file</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="72b40-113">Esse comando importa uma API do arquivo Swagger especificado.</span><span class="sxs-lookup"><span data-stu-id="72b40-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="72b40-114">Exemplo 3: importar uma API de um link WADL</span><span class="sxs-lookup"><span data-stu-id="72b40-114">Example 3: Import an API from a WADL link</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="72b40-115">Esse comando importa uma API do link WADL especificado.</span><span class="sxs-lookup"><span data-stu-id="72b40-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="72b40-116">OS</span><span class="sxs-lookup"><span data-stu-id="72b40-116">PARAMETERS</span></span>

### <span data-ttu-id="72b40-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="72b40-117">-ApiId</span></span>
<span data-ttu-id="72b40-118">Especifica uma ID para a API a ser importada.</span><span class="sxs-lookup"><span data-stu-id="72b40-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="72b40-119">Se você não especificar esse parâmetro, uma ID será gerada para você.</span><span class="sxs-lookup"><span data-stu-id="72b40-119">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b40-120">-ApiType</span><span class="sxs-lookup"><span data-stu-id="72b40-120">-ApiType</span></span>
<span data-ttu-id="72b40-121">Esse parâmetro é opcional com um valor padrão de http.</span><span class="sxs-lookup"><span data-stu-id="72b40-121">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="72b40-122">A opção SOAP só se aplica ao importar WSDL e criar uma API de passagem SOAP.</span><span class="sxs-lookup"><span data-stu-id="72b40-122">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: PsApiManagementApiType
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b40-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="72b40-123">-Context</span></span>
<span data-ttu-id="72b40-124">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="72b40-124">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b40-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72b40-125">-DefaultProfile</span></span>
<span data-ttu-id="72b40-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="72b40-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b40-127">-Caminho</span><span class="sxs-lookup"><span data-stu-id="72b40-127">-Path</span></span>
<span data-ttu-id="72b40-128">Especifica um caminho de API Web como a última parte da URL pública da API.</span><span class="sxs-lookup"><span data-stu-id="72b40-128">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="72b40-129">Essa URL é usada por consumidores de API para enviar solicitações ao serviço Web.</span><span class="sxs-lookup"><span data-stu-id="72b40-129">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="72b40-130">Deve ter de 1 a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="72b40-130">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="72b40-131">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="72b40-131">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b40-132">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="72b40-132">-SpecificationFormat</span></span>
<span data-ttu-id="72b40-133">Especifica o formato de especificação.</span><span class="sxs-lookup"><span data-stu-id="72b40-133">Specifies the specification format.</span></span>
<span data-ttu-id="72b40-134">psdx_paramvalues WADL, WSDL e Swagger.</span><span class="sxs-lookup"><span data-stu-id="72b40-134">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b40-135">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="72b40-135">-SpecificationPath</span></span>
<span data-ttu-id="72b40-136">Especifica o caminho do arquivo de especificação.</span><span class="sxs-lookup"><span data-stu-id="72b40-136">Specifies the specification file path.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromLocalFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b40-137">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="72b40-137">-SpecificationUrl</span></span>
<span data-ttu-id="72b40-138">Especifica a URL de especificação.</span><span class="sxs-lookup"><span data-stu-id="72b40-138">Specifies the specification URL.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromUrl
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b40-139">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="72b40-139">-WsdlEndpointName</span></span>
<span data-ttu-id="72b40-140">Nome local do ponto de extremidade (porta) WSDL a ser importado.</span><span class="sxs-lookup"><span data-stu-id="72b40-140">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="72b40-141">Deve ter de 1 a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="72b40-141">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="72b40-142">Esse parâmetro é opcional e só é necessário para importar WSDL.</span><span class="sxs-lookup"><span data-stu-id="72b40-142">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="72b40-143">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="72b40-143">Default value is $null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b40-144">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="72b40-144">-WsdlServiceName</span></span>
<span data-ttu-id="72b40-145">Nome local do serviço WSDL a ser importado.</span><span class="sxs-lookup"><span data-stu-id="72b40-145">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="72b40-146">Deve ter de 1 a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="72b40-146">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="72b40-147">Esse parâmetro é opcional e só é necessário para importar WSDL.</span><span class="sxs-lookup"><span data-stu-id="72b40-147">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="72b40-148">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="72b40-148">Default value is $null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b40-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b40-149">CommonParameters</span></span>
<span data-ttu-id="72b40-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72b40-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b40-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72b40-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b40-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72b40-152">INPUTS</span></span>

### <span data-ttu-id="72b40-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="72b40-153">None</span></span>
<span data-ttu-id="72b40-154">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="72b40-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72b40-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72b40-155">OUTPUTS</span></span>

### <span data-ttu-id="72b40-156">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="72b40-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="72b40-157">Esse cmdlet retorna a API importada como um objeto **PsApiManagementApi** .</span><span class="sxs-lookup"><span data-stu-id="72b40-157">This cmdlet returns the imported API as a **PsApiManagementApi** object.</span></span>

## <span data-ttu-id="72b40-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72b40-158">NOTES</span></span>

## <span data-ttu-id="72b40-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72b40-159">RELATED LINKS</span></span>

[<span data-ttu-id="72b40-160">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="72b40-160">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="72b40-161">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="72b40-161">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="72b40-162">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="72b40-162">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="72b40-163">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="72b40-163">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="72b40-164">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="72b40-164">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


