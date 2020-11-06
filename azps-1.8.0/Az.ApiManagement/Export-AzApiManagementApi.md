---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 1c322669431377b96f0bc45e1228c52ba70c6d68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595703"
---
# <span data-ttu-id="3cc3a-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3cc3a-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="3cc3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3cc3a-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc3a-103">Exporta uma API para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-103">Exports an API to a file.</span></span>

## <span data-ttu-id="3cc3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3cc3a-104">SYNTAX</span></span>

### <span data-ttu-id="3cc3a-105">ExportToPipeline (padrão)</span><span class="sxs-lookup"><span data-stu-id="3cc3a-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cc3a-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="3cc3a-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cc3a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3cc3a-107">DESCRIPTION</span></span>
<span data-ttu-id="3cc3a-108">O cmdlet **Export-AzApiManagementApi** exporta uma API de gerenciamento de API do Azure para um arquivo em um dos formatos com suporte.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="3cc3a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3cc3a-109">EXAMPLES</span></span>

### <span data-ttu-id="3cc3a-110">Exemplo 1: exportar uma API no formato WADL (linguagem de descrição de aplicativo Web)</span><span class="sxs-lookup"><span data-stu-id="3cc3a-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="3cc3a-111">Esse comando exporta uma API para um arquivo WADL.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="3cc3a-112">OS</span><span class="sxs-lookup"><span data-stu-id="3cc3a-112">PARAMETERS</span></span>

### <span data-ttu-id="3cc3a-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3cc3a-113">-ApiId</span></span>
<span data-ttu-id="3cc3a-114">Especifica a ID da API a ser exportada.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="3cc3a-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="3cc3a-115">-ApiRevision</span></span>
<span data-ttu-id="3cc3a-116">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-116">Identifier of API Revision.</span></span> <span data-ttu-id="3cc3a-117">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-117">This parameter is optional.</span></span> <span data-ttu-id="3cc3a-118">Se não for especificado, a exportação será feita para a revisão de API ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-118">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="3cc3a-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3cc3a-119">-Context</span></span>
<span data-ttu-id="3cc3a-120">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3cc3a-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3cc3a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc3a-121">-DefaultProfile</span></span>
<span data-ttu-id="3cc3a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cc3a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="3cc3a-123">-Force</span></span>
<span data-ttu-id="3cc3a-124">Indica que essa operação substitui o arquivo com o mesmo nome se já existir.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-124">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="3cc3a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cc3a-125">-PassThru</span></span>
<span data-ttu-id="3cc3a-126">Indica que essa operação retorna $True se a API for exportada com êxito ou $False de outra forma.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-126">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="3cc3a-127">-Salvar como</span><span class="sxs-lookup"><span data-stu-id="3cc3a-127">-SaveAs</span></span>
<span data-ttu-id="3cc3a-128">Especifica o caminho de arquivo para o qual salvar a API exportada.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-128">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="3cc3a-129">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="3cc3a-129">-SpecificationFormat</span></span>
<span data-ttu-id="3cc3a-130">Especifica o formato da API.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-130">Specifies the API format.</span></span>
<span data-ttu-id="3cc3a-131">psdx_paramvalues WADL e Swagger.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-131">psdx_paramvalues Wadl and Swagger.</span></span>

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

### <span data-ttu-id="3cc3a-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3cc3a-132">-Confirm</span></span>
<span data-ttu-id="3cc3a-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cc3a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cc3a-134">-WhatIf</span></span>
<span data-ttu-id="3cc3a-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cc3a-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cc3a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc3a-137">CommonParameters</span></span>
<span data-ttu-id="3cc3a-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc3a-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cc3a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc3a-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3cc3a-140">INPUTS</span></span>

### <span data-ttu-id="3cc3a-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3cc3a-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3cc3a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3cc3a-142">System.String</span></span>

### <span data-ttu-id="3cc3a-143">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="3cc3a-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="3cc3a-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3cc3a-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3cc3a-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3cc3a-145">OUTPUTS</span></span>

### <span data-ttu-id="3cc3a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3cc3a-146">System.String</span></span>

## <span data-ttu-id="3cc3a-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3cc3a-147">NOTES</span></span>

## <span data-ttu-id="3cc3a-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3cc3a-148">RELATED LINKS</span></span>

[<span data-ttu-id="3cc3a-149">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3cc3a-149">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="3cc3a-150">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3cc3a-150">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="3cc3a-151">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3cc3a-151">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="3cc3a-152">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3cc3a-152">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="3cc3a-153">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3cc3a-153">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


