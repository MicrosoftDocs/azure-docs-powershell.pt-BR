---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941959"
---
# <span data-ttu-id="e69ed-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e69ed-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="e69ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e69ed-102">SYNOPSIS</span></span>
<span data-ttu-id="e69ed-103">Exporta uma API para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="e69ed-103">Exports an API to a file.</span></span>

## <span data-ttu-id="e69ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e69ed-104">SYNTAX</span></span>

### <span data-ttu-id="e69ed-105">ExportToPipeline (padrão)</span><span class="sxs-lookup"><span data-stu-id="e69ed-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e69ed-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="e69ed-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e69ed-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e69ed-107">DESCRIPTION</span></span>
<span data-ttu-id="e69ed-108">O cmdlet **Export-AzApiManagementApi** exporta uma API de gerenciamento de API do Azure para um arquivo em um dos formatos com suporte.</span><span class="sxs-lookup"><span data-stu-id="e69ed-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="e69ed-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e69ed-109">EXAMPLES</span></span>

### <span data-ttu-id="e69ed-110">Exemplo 1: exportar uma API no formato WADL (linguagem de descrição de aplicativo Web)</span><span class="sxs-lookup"><span data-stu-id="e69ed-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="e69ed-111">Esse comando exporta uma API para um arquivo WADL.</span><span class="sxs-lookup"><span data-stu-id="e69ed-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="e69ed-112">Exemplo 2: exportar uma API no formato de especificação OpenApi 3,0 como documento JSON</span><span class="sxs-lookup"><span data-stu-id="e69ed-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="e69ed-113">Este comando exporta as definições de API no formato Open API como documento JSON</span><span class="sxs-lookup"><span data-stu-id="e69ed-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="e69ed-114">OS</span><span class="sxs-lookup"><span data-stu-id="e69ed-114">PARAMETERS</span></span>

### <span data-ttu-id="e69ed-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e69ed-115">-ApiId</span></span>
<span data-ttu-id="e69ed-116">Especifica a ID da API a ser exportada.</span><span class="sxs-lookup"><span data-stu-id="e69ed-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="e69ed-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e69ed-117">-ApiRevision</span></span>
<span data-ttu-id="e69ed-118">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="e69ed-118">Identifier of API Revision.</span></span> <span data-ttu-id="e69ed-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e69ed-119">This parameter is optional.</span></span> <span data-ttu-id="e69ed-120">Se não for especificado, a exportação será feita para a revisão de API ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="e69ed-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="e69ed-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e69ed-121">-Context</span></span>
<span data-ttu-id="e69ed-122">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e69ed-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e69ed-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e69ed-123">-DefaultProfile</span></span>
<span data-ttu-id="e69ed-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e69ed-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e69ed-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e69ed-125">-Force</span></span>
<span data-ttu-id="e69ed-126">Indica que essa operação substitui o arquivo com o mesmo nome se já existir.</span><span class="sxs-lookup"><span data-stu-id="e69ed-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e69ed-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e69ed-127">-PassThru</span></span>
<span data-ttu-id="e69ed-128">Indica que essa operação retorna $True se a API for exportada com êxito ou $False de outra forma.</span><span class="sxs-lookup"><span data-stu-id="e69ed-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e69ed-129">-Salvar como</span><span class="sxs-lookup"><span data-stu-id="e69ed-129">-SaveAs</span></span>
<span data-ttu-id="e69ed-130">Especifica o caminho de arquivo para o qual salvar a API exportada.</span><span class="sxs-lookup"><span data-stu-id="e69ed-130">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e69ed-131">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="e69ed-131">-SpecificationFormat</span></span>
<span data-ttu-id="e69ed-132">Especifica o formato da API.</span><span class="sxs-lookup"><span data-stu-id="e69ed-132">Specifies the API format.</span></span>
<span data-ttu-id="e69ed-133">psdx_paramvalues WADL, WSDL, Swagger, OpenApi e OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="e69ed-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

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

### <span data-ttu-id="e69ed-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e69ed-134">-Confirm</span></span>
<span data-ttu-id="e69ed-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e69ed-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e69ed-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e69ed-136">-WhatIf</span></span>
<span data-ttu-id="e69ed-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e69ed-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e69ed-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e69ed-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e69ed-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e69ed-139">CommonParameters</span></span>
<span data-ttu-id="e69ed-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e69ed-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e69ed-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e69ed-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e69ed-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e69ed-142">INPUTS</span></span>

### <span data-ttu-id="e69ed-143">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e69ed-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e69ed-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e69ed-144">System.String</span></span>

### <span data-ttu-id="e69ed-145">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="e69ed-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="e69ed-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e69ed-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e69ed-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e69ed-147">OUTPUTS</span></span>

### <span data-ttu-id="e69ed-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e69ed-148">System.String</span></span>

## <span data-ttu-id="e69ed-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e69ed-149">NOTES</span></span>

## <span data-ttu-id="e69ed-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e69ed-150">RELATED LINKS</span></span>

[<span data-ttu-id="e69ed-151">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e69ed-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="e69ed-152">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e69ed-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="e69ed-153">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e69ed-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="e69ed-154">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e69ed-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="e69ed-155">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e69ed-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


