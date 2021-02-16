---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113658"
---
# <span data-ttu-id="76912-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="76912-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="76912-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76912-102">SYNOPSIS</span></span>
<span data-ttu-id="76912-103">Exporta uma API para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="76912-103">Exports an API to a file.</span></span>

## <span data-ttu-id="76912-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76912-104">SYNTAX</span></span>

### <span data-ttu-id="76912-105">ExportToPipeline (Padrão)</span><span class="sxs-lookup"><span data-stu-id="76912-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76912-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="76912-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76912-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="76912-107">DESCRIPTION</span></span>
<span data-ttu-id="76912-108">O cmdlet **Export-AzApiManagementApi** exporta uma API de gerenciamento de API do Azure para um arquivo em um dos formatos com suporte.</span><span class="sxs-lookup"><span data-stu-id="76912-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="76912-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="76912-109">EXAMPLES</span></span>

### <span data-ttu-id="76912-110">Exemplo 1: Exportar uma API no formato de Linguagem de Descrição de Aplicativo Web (WADEL)</span><span class="sxs-lookup"><span data-stu-id="76912-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="76912-111">Esse comando exporta uma API para um arquivo WADEL.</span><span class="sxs-lookup"><span data-stu-id="76912-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="76912-112">Exemplo 2: Exportar uma API no Formato de Especificação OpenApi 3.0 como Documento Json</span><span class="sxs-lookup"><span data-stu-id="76912-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="76912-113">Este comando exporta definições de API no formato Open Api como documento Json</span><span class="sxs-lookup"><span data-stu-id="76912-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="76912-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76912-114">PARAMETERS</span></span>

### <span data-ttu-id="76912-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="76912-115">-ApiId</span></span>
<span data-ttu-id="76912-116">Especifica a ID da API a ser exportada.</span><span class="sxs-lookup"><span data-stu-id="76912-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="76912-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="76912-117">-ApiRevision</span></span>
<span data-ttu-id="76912-118">Identificador de Revisão da API.</span><span class="sxs-lookup"><span data-stu-id="76912-118">Identifier of API Revision.</span></span> <span data-ttu-id="76912-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="76912-119">This parameter is optional.</span></span> <span data-ttu-id="76912-120">Se não especificado, a exportação será feita para a revisão da api ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="76912-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="76912-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="76912-121">-Context</span></span>
<span data-ttu-id="76912-122">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="76912-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="76912-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76912-123">-DefaultProfile</span></span>
<span data-ttu-id="76912-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="76912-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76912-125">-Forçar</span><span class="sxs-lookup"><span data-stu-id="76912-125">-Force</span></span>
<span data-ttu-id="76912-126">Indica que essa operação substitui o arquivo do mesmo nome se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="76912-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="76912-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76912-127">-PassThru</span></span>
<span data-ttu-id="76912-128">Indica que essa operação retorna $True se a API for exportada com êxito ou $False contrário.</span><span class="sxs-lookup"><span data-stu-id="76912-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="76912-129">-SalvarAs</span><span class="sxs-lookup"><span data-stu-id="76912-129">-SaveAs</span></span>
<span data-ttu-id="76912-130">Especifica o caminho do arquivo para o qual salvar a API exportada.</span><span class="sxs-lookup"><span data-stu-id="76912-130">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="76912-131">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="76912-131">-SpecificationFormat</span></span>
<span data-ttu-id="76912-132">Especifica o formato da API.</span><span class="sxs-lookup"><span data-stu-id="76912-132">Specifies the API format.</span></span>
<span data-ttu-id="76912-133">psdx_paramvalues, Wsdl, Wade, OpenApi e OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="76912-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

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

### <span data-ttu-id="76912-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="76912-134">-Confirm</span></span>
<span data-ttu-id="76912-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76912-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76912-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76912-136">-WhatIf</span></span>
<span data-ttu-id="76912-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="76912-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76912-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76912-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76912-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76912-139">CommonParameters</span></span>
<span data-ttu-id="76912-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76912-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76912-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76912-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76912-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="76912-142">INPUTS</span></span>

### <span data-ttu-id="76912-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="76912-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="76912-144">System.String</span><span class="sxs-lookup"><span data-stu-id="76912-144">System.String</span></span>

### <span data-ttu-id="76912-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="76912-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="76912-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="76912-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="76912-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="76912-147">OUTPUTS</span></span>

### <span data-ttu-id="76912-148">System.String</span><span class="sxs-lookup"><span data-stu-id="76912-148">System.String</span></span>

## <span data-ttu-id="76912-149">Notas</span><span class="sxs-lookup"><span data-stu-id="76912-149">NOTES</span></span>

## <span data-ttu-id="76912-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76912-150">RELATED LINKS</span></span>

[<span data-ttu-id="76912-151">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="76912-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="76912-152">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="76912-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="76912-153">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="76912-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="76912-154">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="76912-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="76912-155">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="76912-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


