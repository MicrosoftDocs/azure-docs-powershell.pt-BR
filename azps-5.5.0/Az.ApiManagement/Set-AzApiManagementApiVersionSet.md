---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118037"
---
# <span data-ttu-id="293fd-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="293fd-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="293fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="293fd-102">SYNOPSIS</span></span>
<span data-ttu-id="293fd-103">Atualiza um Conjunto de Versão da API no Contexto de Gerenciamento da API.</span><span class="sxs-lookup"><span data-stu-id="293fd-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="293fd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="293fd-104">SYNTAX</span></span>

### <span data-ttu-id="293fd-105">ExpandedParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="293fd-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="293fd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="293fd-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="293fd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="293fd-107">DESCRIPTION</span></span>

<span data-ttu-id="293fd-108">O cmdlet **Set-AzApiManagementApiVersionSet** modifica um conjunto de versões da API de gerenciamento da API do Azure.</span><span class="sxs-lookup"><span data-stu-id="293fd-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="293fd-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="293fd-109">EXAMPLES</span></span>

### <span data-ttu-id="293fd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="293fd-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="293fd-111">Esse comando atualiza um conjunto de versões da API existente com esquema de controle de versão `Header` e parâmetro de `api-version` Header.</span><span class="sxs-lookup"><span data-stu-id="293fd-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="293fd-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="293fd-112">PARAMETERS</span></span>

### <span data-ttu-id="293fd-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="293fd-113">-ApiVersionSetId</span></span>
<span data-ttu-id="293fd-114">Identificador do novo Conjunto de Versões da API.</span><span class="sxs-lookup"><span data-stu-id="293fd-114">Identifier for new API Version Set.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="293fd-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="293fd-115">-Context</span></span>
<span data-ttu-id="293fd-116">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="293fd-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="293fd-117">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="293fd-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="293fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293fd-118">-DefaultProfile</span></span>
<span data-ttu-id="293fd-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="293fd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="293fd-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="293fd-120">-Description</span></span>
<span data-ttu-id="293fd-121">Descrição do conjunto de versões da Api.</span><span class="sxs-lookup"><span data-stu-id="293fd-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="293fd-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="293fd-122">-HeaderName</span></span>
<span data-ttu-id="293fd-123">O valor do Header que conterá as informações de versão.</span><span class="sxs-lookup"><span data-stu-id="293fd-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="293fd-124">Se o HEADER do Esquema de Versão for escolhido, esse valor deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="293fd-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="293fd-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="293fd-125">-InputObject</span></span>
<span data-ttu-id="293fd-126">Instância do PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="293fd-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="293fd-127">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="293fd-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="293fd-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="293fd-128">-Name</span></span>
<span data-ttu-id="293fd-129">O nome do Conjunto apiVersion.</span><span class="sxs-lookup"><span data-stu-id="293fd-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="293fd-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="293fd-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="293fd-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="293fd-131">-PassThru</span></span>
<span data-ttu-id="293fd-132">Se especificado, a instância do Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet que representa o apiVersionSet modificado será escrita em saída.</span><span class="sxs-lookup"><span data-stu-id="293fd-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293fd-133">-Nomeda Consulta</span><span class="sxs-lookup"><span data-stu-id="293fd-133">-QueryName</span></span>
<span data-ttu-id="293fd-134">O valor da consulta que conterá as informações de versão.</span><span class="sxs-lookup"><span data-stu-id="293fd-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="293fd-135">Se a Consulta esquema de versão for escolhida, esse valor deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="293fd-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="293fd-136">-Esquema</span><span class="sxs-lookup"><span data-stu-id="293fd-136">-Scheme</span></span>
<span data-ttu-id="293fd-137">Esquema de versionamento para selecionar para o Conjunto de Versão da Api.</span><span class="sxs-lookup"><span data-stu-id="293fd-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="293fd-138">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="293fd-138">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="293fd-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="293fd-139">-Confirm</span></span>
<span data-ttu-id="293fd-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="293fd-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="293fd-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="293fd-141">-WhatIf</span></span>
<span data-ttu-id="293fd-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="293fd-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="293fd-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="293fd-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="293fd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293fd-144">CommonParameters</span></span>
<span data-ttu-id="293fd-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="293fd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293fd-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="293fd-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293fd-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="293fd-147">INPUTS</span></span>

### <span data-ttu-id="293fd-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="293fd-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="293fd-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="293fd-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="293fd-150">System.String</span><span class="sxs-lookup"><span data-stu-id="293fd-150">System.String</span></span>

### <span data-ttu-id="293fd-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="293fd-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="293fd-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="293fd-152">OUTPUTS</span></span>

### <span data-ttu-id="293fd-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="293fd-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="293fd-154">Notas</span><span class="sxs-lookup"><span data-stu-id="293fd-154">NOTES</span></span>

## <span data-ttu-id="293fd-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="293fd-155">RELATED LINKS</span></span>

[<span data-ttu-id="293fd-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="293fd-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="293fd-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="293fd-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="293fd-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="293fd-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
