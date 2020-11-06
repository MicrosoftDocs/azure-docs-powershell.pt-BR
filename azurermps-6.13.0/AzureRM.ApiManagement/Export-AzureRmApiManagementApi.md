---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/export-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 7dc06f280595551a9e054c251339e96163b798b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602811"
---
# <span data-ttu-id="03bd1-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="03bd1-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="03bd1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03bd1-102">SYNOPSIS</span></span>
<span data-ttu-id="03bd1-103">Exporta uma API para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="03bd1-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03bd1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03bd1-104">SYNTAX</span></span>

### <span data-ttu-id="03bd1-105">ExportToPipeline (padrão)</span><span class="sxs-lookup"><span data-stu-id="03bd1-105">ExportToPipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03bd1-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="03bd1-106">ExportToFile</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03bd1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="03bd1-107">DESCRIPTION</span></span>
<span data-ttu-id="03bd1-108">O cmdlet **Export-AzureRmApiManagementApi** exporta uma API de gerenciamento de API do Azure para um arquivo em um dos formatos com suporte.</span><span class="sxs-lookup"><span data-stu-id="03bd1-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="03bd1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03bd1-109">EXAMPLES</span></span>

### <span data-ttu-id="03bd1-110">Exemplo 1: exportar uma API no formato WADL (linguagem de descrição de aplicativo Web)</span><span class="sxs-lookup"><span data-stu-id="03bd1-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="03bd1-111">Esse comando exporta uma API para um arquivo WADL.</span><span class="sxs-lookup"><span data-stu-id="03bd1-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="03bd1-112">OS</span><span class="sxs-lookup"><span data-stu-id="03bd1-112">PARAMETERS</span></span>

### <span data-ttu-id="03bd1-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="03bd1-113">-ApiId</span></span>
<span data-ttu-id="03bd1-114">Especifica a ID da API a ser exportada.</span><span class="sxs-lookup"><span data-stu-id="03bd1-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="03bd1-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="03bd1-115">-ApiRevision</span></span>
<span data-ttu-id="03bd1-116">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="03bd1-116">Identifier of API Revision.</span></span> <span data-ttu-id="03bd1-117">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="03bd1-117">This parameter is optional.</span></span> <span data-ttu-id="03bd1-118">Se não for especificado, a exportação será feita para a revisão de API ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="03bd1-118">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="03bd1-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="03bd1-119">-Context</span></span>
<span data-ttu-id="03bd1-120">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="03bd1-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="03bd1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03bd1-121">-DefaultProfile</span></span>
<span data-ttu-id="03bd1-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03bd1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bd1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="03bd1-123">-Force</span></span>
<span data-ttu-id="03bd1-124">Indica que essa operação substitui o arquivo com o mesmo nome se já existir.</span><span class="sxs-lookup"><span data-stu-id="03bd1-124">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="03bd1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03bd1-125">-PassThru</span></span>
<span data-ttu-id="03bd1-126">Indica que essa operação retorna $True se a API for exportada com êxito ou $False de outra forma.</span><span class="sxs-lookup"><span data-stu-id="03bd1-126">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="03bd1-127">-Salvar como</span><span class="sxs-lookup"><span data-stu-id="03bd1-127">-SaveAs</span></span>
<span data-ttu-id="03bd1-128">Especifica o caminho de arquivo para o qual salvar a API exportada.</span><span class="sxs-lookup"><span data-stu-id="03bd1-128">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="03bd1-129">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="03bd1-129">-SpecificationFormat</span></span>
<span data-ttu-id="03bd1-130">Especifica o formato da API.</span><span class="sxs-lookup"><span data-stu-id="03bd1-130">Specifies the API format.</span></span>
<span data-ttu-id="03bd1-131">psdx_paramvalues WADL e Swagger.</span><span class="sxs-lookup"><span data-stu-id="03bd1-131">psdx_paramvalues Wadl and Swagger.</span></span>

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

### <span data-ttu-id="03bd1-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="03bd1-132">-Confirm</span></span>
<span data-ttu-id="03bd1-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03bd1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03bd1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03bd1-134">-WhatIf</span></span>
<span data-ttu-id="03bd1-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="03bd1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03bd1-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="03bd1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03bd1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bd1-137">CommonParameters</span></span>
<span data-ttu-id="03bd1-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03bd1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bd1-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03bd1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bd1-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="03bd1-140">INPUTS</span></span>

### <span data-ttu-id="03bd1-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="03bd1-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="03bd1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="03bd1-142">System.String</span></span>

### <span data-ttu-id="03bd1-143">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="03bd1-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="03bd1-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="03bd1-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="03bd1-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="03bd1-145">OUTPUTS</span></span>

### <span data-ttu-id="03bd1-146">System. String</span><span class="sxs-lookup"><span data-stu-id="03bd1-146">System.String</span></span>
<span data-ttu-id="03bd1-147">Esse cmdlet retorna o conteúdo da API exportado como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="03bd1-147">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="03bd1-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="03bd1-148">NOTES</span></span>

## <span data-ttu-id="03bd1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03bd1-149">RELATED LINKS</span></span>

[<span data-ttu-id="03bd1-150">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="03bd1-150">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="03bd1-151">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="03bd1-151">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="03bd1-152">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="03bd1-152">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="03bd1-153">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="03bd1-153">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="03bd1-154">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="03bd1-154">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


