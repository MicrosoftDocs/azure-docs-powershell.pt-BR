---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 126f30e732bc9c55c78c94d6c802b05a18ce29db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890678"
---
# <span data-ttu-id="e12c1-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e12c1-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="e12c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e12c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e12c1-103">Cria um conjunto de versão da API.</span><span class="sxs-lookup"><span data-stu-id="e12c1-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="e12c1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e12c1-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e12c1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e12c1-105">DESCRIPTION</span></span>
<span data-ttu-id="e12c1-106">O cmdlet **New-AzApiManagementApiVersionSet** cria uma entidade de conjunto de versão da API no contexto de Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="e12c1-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="e12c1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e12c1-107">EXAMPLES</span></span>

### <span data-ttu-id="e12c1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e12c1-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

ApiVersionSetId   : ea9a87cd-a699-4a75-bf7d-909846b91268
Description       : version by xmsversion
VersionQueryName  :
VersionHeaderName : x-ms-version
DisplayName       : newversion
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/ea9a87cd-a699-4a75-bf7d-909846b91268
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="e12c1-109">Este comando cria um Conjunto de Versão da API que esquema de controle de versão `Query` e parâmetro de consulta `api-version` .</span><span class="sxs-lookup"><span data-stu-id="e12c1-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="e12c1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e12c1-110">PARAMETERS</span></span>

### <span data-ttu-id="e12c1-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="e12c1-111">-ApiVersionSetId</span></span>
<span data-ttu-id="e12c1-112">Identificador do novo Conjunto de Versão da API.</span><span class="sxs-lookup"><span data-stu-id="e12c1-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="e12c1-113">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e12c1-113">This parameter is optional.</span></span>
<span data-ttu-id="e12c1-114">Se não for especificado, um identificador será gerado.</span><span class="sxs-lookup"><span data-stu-id="e12c1-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="e12c1-115">-Context</span><span class="sxs-lookup"><span data-stu-id="e12c1-115">-Context</span></span>
<span data-ttu-id="e12c1-116">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e12c1-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e12c1-117">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e12c1-117">This parameter is required.</span></span>

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

### <span data-ttu-id="e12c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e12c1-118">-DefaultProfile</span></span>
<span data-ttu-id="e12c1-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e12c1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e12c1-120">-Description</span><span class="sxs-lookup"><span data-stu-id="e12c1-120">-Description</span></span>
<span data-ttu-id="e12c1-121">Descrição do conjunto de versão da Api.</span><span class="sxs-lookup"><span data-stu-id="e12c1-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="e12c1-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="e12c1-122">-HeaderName</span></span>
<span data-ttu-id="e12c1-123">O valor do Header que conterá as informações de versão.</span><span class="sxs-lookup"><span data-stu-id="e12c1-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="e12c1-124">Se o HEADER do Esquema de Versão for escolhido, esse valor deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="e12c1-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="e12c1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e12c1-125">-Name</span></span>
<span data-ttu-id="e12c1-126">O nome do Conjunto ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="e12c1-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="e12c1-127">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e12c1-127">This parameter is required.</span></span>

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

### <span data-ttu-id="e12c1-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="e12c1-128">-QueryName</span></span>
<span data-ttu-id="e12c1-129">O valor de consulta que conterá as informações de versão.</span><span class="sxs-lookup"><span data-stu-id="e12c1-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="e12c1-130">Se a consulta esquema de versão for escolhida, esse valor deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="e12c1-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="e12c1-131">-Scheme</span><span class="sxs-lookup"><span data-stu-id="e12c1-131">-Scheme</span></span>
<span data-ttu-id="e12c1-132">Esquema de versão a ser selecionado para o Conjunto de Versão da Api.</span><span class="sxs-lookup"><span data-stu-id="e12c1-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="e12c1-133">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e12c1-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e12c1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e12c1-134">-Confirm</span></span>
<span data-ttu-id="e12c1-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e12c1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e12c1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e12c1-136">-WhatIf</span></span>
<span data-ttu-id="e12c1-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e12c1-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e12c1-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e12c1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e12c1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e12c1-139">CommonParameters</span></span>
<span data-ttu-id="e12c1-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e12c1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e12c1-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e12c1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e12c1-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e12c1-142">INPUTS</span></span>

### <span data-ttu-id="e12c1-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e12c1-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e12c1-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e12c1-144">System.String</span></span>

### <span data-ttu-id="e12c1-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="e12c1-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="e12c1-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e12c1-146">OUTPUTS</span></span>

### <span data-ttu-id="e12c1-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e12c1-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="e12c1-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="e12c1-148">NOTES</span></span>

## <span data-ttu-id="e12c1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e12c1-149">RELATED LINKS</span></span>

[<span data-ttu-id="e12c1-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e12c1-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="e12c1-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e12c1-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="e12c1-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e12c1-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)