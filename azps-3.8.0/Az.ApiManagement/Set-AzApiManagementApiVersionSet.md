---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943862"
---
# <span data-ttu-id="450c9-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="450c9-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="450c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="450c9-102">SYNOPSIS</span></span>
<span data-ttu-id="450c9-103">Atualiza uma versão de API definida no contexto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="450c9-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="450c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="450c9-104">SYNTAX</span></span>

### <span data-ttu-id="450c9-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="450c9-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="450c9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="450c9-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="450c9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="450c9-107">DESCRIPTION</span></span>

<span data-ttu-id="450c9-108">O cmdlet **set-AzApiManagementApiVersionSet** modifica um conjunto de versões da API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="450c9-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="450c9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="450c9-109">EXAMPLES</span></span>

### <span data-ttu-id="450c9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="450c9-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="450c9-111">Esse comando atualiza uma versão de API existente definida com o parâmetro de cabeçalho e esquema de controle de versão `Header` `api-version` .</span><span class="sxs-lookup"><span data-stu-id="450c9-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="450c9-112">OS</span><span class="sxs-lookup"><span data-stu-id="450c9-112">PARAMETERS</span></span>

### <span data-ttu-id="450c9-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="450c9-113">-ApiVersionSetId</span></span>
<span data-ttu-id="450c9-114">Identificador para o novo conjunto de versões da API.</span><span class="sxs-lookup"><span data-stu-id="450c9-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="450c9-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="450c9-115">-Context</span></span>
<span data-ttu-id="450c9-116">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="450c9-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="450c9-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="450c9-117">This parameter is required.</span></span>

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

### <span data-ttu-id="450c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450c9-118">-DefaultProfile</span></span>
<span data-ttu-id="450c9-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="450c9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="450c9-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="450c9-120">-Description</span></span>
<span data-ttu-id="450c9-121">Descrição do conjunto de versões da API.</span><span class="sxs-lookup"><span data-stu-id="450c9-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="450c9-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="450c9-122">-HeaderName</span></span>
<span data-ttu-id="450c9-123">O valor de cabeçalho que conterá as informações de controle de versão.</span><span class="sxs-lookup"><span data-stu-id="450c9-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="450c9-124">Se o cabeçalho do esquema de controle de versão for escolhido, esse valor deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="450c9-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="450c9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="450c9-125">-InputObject</span></span>
<span data-ttu-id="450c9-126">Instância do PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="450c9-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="450c9-127">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="450c9-127">This parameter is required.</span></span>

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

### <span data-ttu-id="450c9-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="450c9-128">-Name</span></span>
<span data-ttu-id="450c9-129">O nome do conjunto de ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="450c9-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="450c9-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="450c9-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="450c9-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="450c9-131">-PassThru</span></span>
<span data-ttu-id="450c9-132">Se especificado, a instância do tipo Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiVersionSet que representa o apiVersionSet modificado será gravada para output.</span><span class="sxs-lookup"><span data-stu-id="450c9-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="450c9-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="450c9-133">-QueryName</span></span>
<span data-ttu-id="450c9-134">O valor da consulta que conterá as informações de controle de versão.</span><span class="sxs-lookup"><span data-stu-id="450c9-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="450c9-135">Se consulta do esquema de controle de versão for escolhida, esse valor deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="450c9-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="450c9-136">-Esquema</span><span class="sxs-lookup"><span data-stu-id="450c9-136">-Scheme</span></span>
<span data-ttu-id="450c9-137">Esquema de controle de versão para selecionar para o conjunto de versionamento de API.</span><span class="sxs-lookup"><span data-stu-id="450c9-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="450c9-138">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="450c9-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="450c9-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="450c9-139">-Confirm</span></span>
<span data-ttu-id="450c9-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="450c9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="450c9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="450c9-141">-WhatIf</span></span>
<span data-ttu-id="450c9-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="450c9-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="450c9-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="450c9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="450c9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450c9-144">CommonParameters</span></span>
<span data-ttu-id="450c9-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="450c9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450c9-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="450c9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450c9-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="450c9-147">INPUTS</span></span>

### <span data-ttu-id="450c9-148">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="450c9-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="450c9-149">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="450c9-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="450c9-150">System. String</span><span class="sxs-lookup"><span data-stu-id="450c9-150">System.String</span></span>

### <span data-ttu-id="450c9-151">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="450c9-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="450c9-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="450c9-152">OUTPUTS</span></span>

### <span data-ttu-id="450c9-153">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="450c9-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="450c9-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="450c9-154">NOTES</span></span>

## <span data-ttu-id="450c9-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="450c9-155">RELATED LINKS</span></span>

[<span data-ttu-id="450c9-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="450c9-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="450c9-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="450c9-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="450c9-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="450c9-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
