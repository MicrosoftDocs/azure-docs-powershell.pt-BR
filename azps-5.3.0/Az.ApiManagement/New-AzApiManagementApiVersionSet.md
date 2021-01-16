---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 0e007634659d842b0c59712a2ee191a79e1aeb58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432670"
---
# <span data-ttu-id="ca260-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ca260-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="ca260-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca260-102">SYNOPSIS</span></span>
<span data-ttu-id="ca260-103">Cria um conjunto de versões de API.</span><span class="sxs-lookup"><span data-stu-id="ca260-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="ca260-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca260-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca260-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca260-105">DESCRIPTION</span></span>
<span data-ttu-id="ca260-106">O cmdlet **New-AzApiManagementApiVersionSet** cria uma entidade do conjunto de versões da API no contexto de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca260-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="ca260-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca260-107">EXAMPLES</span></span>

### <span data-ttu-id="ca260-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ca260-108">Example 1</span></span>
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

<span data-ttu-id="ca260-109">Esse comando cria uma versão de API que define qual o esquema `Query` de controle de versão e o parâmetro de consulta `api-version` .</span><span class="sxs-lookup"><span data-stu-id="ca260-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="ca260-110">OS</span><span class="sxs-lookup"><span data-stu-id="ca260-110">PARAMETERS</span></span>

### <span data-ttu-id="ca260-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="ca260-111">-ApiVersionSetId</span></span>
<span data-ttu-id="ca260-112">Identificador para o novo conjunto de versões da API.</span><span class="sxs-lookup"><span data-stu-id="ca260-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="ca260-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ca260-113">This parameter is optional.</span></span>
<span data-ttu-id="ca260-114">Se não for especificado um identificador será gerado.</span><span class="sxs-lookup"><span data-stu-id="ca260-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="ca260-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ca260-115">-Context</span></span>
<span data-ttu-id="ca260-116">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ca260-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ca260-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ca260-117">This parameter is required.</span></span>

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

### <span data-ttu-id="ca260-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca260-118">-DefaultProfile</span></span>
<span data-ttu-id="ca260-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca260-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca260-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="ca260-120">-Description</span></span>
<span data-ttu-id="ca260-121">Descrição do conjunto de versões da API.</span><span class="sxs-lookup"><span data-stu-id="ca260-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="ca260-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="ca260-122">-HeaderName</span></span>
<span data-ttu-id="ca260-123">O valor de cabeçalho que conterá as informações de controle de versão.</span><span class="sxs-lookup"><span data-stu-id="ca260-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="ca260-124">Se o cabeçalho do esquema de controle de versão for escolhido, esse valor deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="ca260-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="ca260-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca260-125">-Name</span></span>
<span data-ttu-id="ca260-126">O nome do conjunto de ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="ca260-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="ca260-127">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ca260-127">This parameter is required.</span></span>

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

### <span data-ttu-id="ca260-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="ca260-128">-QueryName</span></span>
<span data-ttu-id="ca260-129">O valor da consulta que conterá as informações de controle de versão.</span><span class="sxs-lookup"><span data-stu-id="ca260-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="ca260-130">Se consulta do esquema de controle de versão for escolhida, esse valor deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="ca260-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="ca260-131">-Esquema</span><span class="sxs-lookup"><span data-stu-id="ca260-131">-Scheme</span></span>
<span data-ttu-id="ca260-132">Esquema de controle de versão para selecionar para o conjunto de versionamento de API.</span><span class="sxs-lookup"><span data-stu-id="ca260-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="ca260-133">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ca260-133">This parameter is required.</span></span>

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

### <span data-ttu-id="ca260-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ca260-134">-Confirm</span></span>
<span data-ttu-id="ca260-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca260-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca260-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca260-136">-WhatIf</span></span>
<span data-ttu-id="ca260-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca260-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca260-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca260-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca260-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca260-139">CommonParameters</span></span>
<span data-ttu-id="ca260-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca260-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca260-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca260-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca260-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca260-142">INPUTS</span></span>

### <span data-ttu-id="ca260-143">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ca260-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ca260-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ca260-144">System.String</span></span>

### <span data-ttu-id="ca260-145">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="ca260-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="ca260-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca260-146">OUTPUTS</span></span>

### <span data-ttu-id="ca260-147">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ca260-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="ca260-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca260-148">NOTES</span></span>

## <span data-ttu-id="ca260-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca260-149">RELATED LINKS</span></span>

[<span data-ttu-id="ca260-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ca260-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="ca260-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ca260-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="ca260-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ca260-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)