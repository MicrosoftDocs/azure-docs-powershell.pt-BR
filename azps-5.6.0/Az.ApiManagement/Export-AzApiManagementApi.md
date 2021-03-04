---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 9f65550f9a3e1aec9e0f44fa2e436f715e23f948
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889589"
---
# <span data-ttu-id="24d29-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="24d29-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="24d29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24d29-102">SYNOPSIS</span></span>
<span data-ttu-id="24d29-103">Exporta uma API para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="24d29-103">Exports an API to a file.</span></span>

## <span data-ttu-id="24d29-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="24d29-104">SYNTAX</span></span>

### <span data-ttu-id="24d29-105">ExportToPipeline (Padrão)</span><span class="sxs-lookup"><span data-stu-id="24d29-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24d29-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="24d29-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24d29-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="24d29-107">DESCRIPTION</span></span>
<span data-ttu-id="24d29-108">O cmdlet **Export-AzApiManagementApi** exporta uma API de Gerenciamento de API do Azure para um arquivo em um dos formatos com suporte.</span><span class="sxs-lookup"><span data-stu-id="24d29-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="24d29-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24d29-109">EXAMPLES</span></span>

### <span data-ttu-id="24d29-110">Exemplo 1: Exportar uma API no formato WADL (Linguagem de Descrição do Aplicativo Web)</span><span class="sxs-lookup"><span data-stu-id="24d29-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="24d29-111">Esse comando exporta uma API para um arquivo WADL.</span><span class="sxs-lookup"><span data-stu-id="24d29-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="24d29-112">Exemplo 2: Exportar uma API no Formato de Especificação OpenApi 3.0 como Documento Json</span><span class="sxs-lookup"><span data-stu-id="24d29-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="24d29-113">Este comando exporta definições de API no formato Api Aberta como documento Json</span><span class="sxs-lookup"><span data-stu-id="24d29-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="24d29-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="24d29-114">PARAMETERS</span></span>

### <span data-ttu-id="24d29-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="24d29-115">-ApiId</span></span>
<span data-ttu-id="24d29-116">Especifica a ID da API a ser exportada.</span><span class="sxs-lookup"><span data-stu-id="24d29-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="24d29-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="24d29-117">-ApiRevision</span></span>
<span data-ttu-id="24d29-118">Identificador da Revisão da API.</span><span class="sxs-lookup"><span data-stu-id="24d29-118">Identifier of API Revision.</span></span> <span data-ttu-id="24d29-119">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="24d29-119">This parameter is optional.</span></span> <span data-ttu-id="24d29-120">Se não for especificado, a exportação será feita para a revisão da api ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="24d29-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="24d29-121">-Context</span><span class="sxs-lookup"><span data-stu-id="24d29-121">-Context</span></span>
<span data-ttu-id="24d29-122">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="24d29-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="24d29-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d29-123">-DefaultProfile</span></span>
<span data-ttu-id="24d29-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="24d29-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24d29-125">-Force</span><span class="sxs-lookup"><span data-stu-id="24d29-125">-Force</span></span>
<span data-ttu-id="24d29-126">Indica que essa operação substitui o arquivo do mesmo nome se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="24d29-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="24d29-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24d29-127">-PassThru</span></span>
<span data-ttu-id="24d29-128">Indica que essa operação retornará $True se a API for exportada com êxito ou $False caso contrário.</span><span class="sxs-lookup"><span data-stu-id="24d29-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="24d29-129">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="24d29-129">-SaveAs</span></span>
<span data-ttu-id="24d29-130">Especifica o caminho do arquivo para o qual salvar a API exportada.</span><span class="sxs-lookup"><span data-stu-id="24d29-130">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="24d29-131">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="24d29-131">-SpecificationFormat</span></span>
<span data-ttu-id="24d29-132">Especifica o formato da API.</span><span class="sxs-lookup"><span data-stu-id="24d29-132">Specifies the API format.</span></span>
<span data-ttu-id="24d29-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi e OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="24d29-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

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

### <span data-ttu-id="24d29-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24d29-134">-Confirm</span></span>
<span data-ttu-id="24d29-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24d29-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24d29-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24d29-136">-WhatIf</span></span>
<span data-ttu-id="24d29-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24d29-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24d29-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24d29-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24d29-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d29-139">CommonParameters</span></span>
<span data-ttu-id="24d29-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24d29-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d29-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24d29-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d29-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24d29-142">INPUTS</span></span>

### <span data-ttu-id="24d29-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="24d29-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="24d29-144">System.String</span><span class="sxs-lookup"><span data-stu-id="24d29-144">System.String</span></span>

### <span data-ttu-id="24d29-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="24d29-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="24d29-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="24d29-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="24d29-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="24d29-147">OUTPUTS</span></span>

### <span data-ttu-id="24d29-148">System.String</span><span class="sxs-lookup"><span data-stu-id="24d29-148">System.String</span></span>

## <span data-ttu-id="24d29-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="24d29-149">NOTES</span></span>

## <span data-ttu-id="24d29-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24d29-150">RELATED LINKS</span></span>

[<span data-ttu-id="24d29-151">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="24d29-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="24d29-152">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="24d29-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="24d29-153">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="24d29-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="24d29-154">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="24d29-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="24d29-155">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="24d29-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


