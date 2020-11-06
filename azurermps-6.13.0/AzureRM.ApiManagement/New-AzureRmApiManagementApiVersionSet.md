---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: e10b91994bdb7351a7154d04cb7de3231ed87a5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428648"
---
# <span data-ttu-id="b4eb3-101">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b4eb3-101">New-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="b4eb3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="b4eb3-103">Cria um conjunto de versões de API.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-103">Creates an API Version Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4eb3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4eb3-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -Name <String> -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4eb3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4eb3-105">DESCRIPTION</span></span>
<span data-ttu-id="b4eb3-106">O cmdlet **New-AzureRmApiManagementApiVersionSet** cria uma entidade do conjunto de versões da API no contexto de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-106">The **New-AzureRmApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="b4eb3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4eb3-107">EXAMPLES</span></span>

### <span data-ttu-id="b4eb3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4eb3-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

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

<span data-ttu-id="b4eb3-109">Esse comando cria uma versão de API que define qual o esquema `Query` de controle de versão e o parâmetro de consulta `api-version` .</span><span class="sxs-lookup"><span data-stu-id="b4eb3-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="b4eb3-110">OS</span><span class="sxs-lookup"><span data-stu-id="b4eb3-110">PARAMETERS</span></span>

### <span data-ttu-id="b4eb3-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="b4eb3-111">-ApiVersionSetId</span></span>
<span data-ttu-id="b4eb3-112">Identificador para o novo conjunto de versões da API.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="b4eb3-113">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-113">This parameter is optional.</span></span>
<span data-ttu-id="b4eb3-114">Se não for especificado um identificador será gerado.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="b4eb3-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="b4eb3-115">-Context</span></span>
<span data-ttu-id="b4eb3-116">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b4eb3-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-117">This parameter is required.</span></span>

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

### <span data-ttu-id="b4eb3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4eb3-118">-DefaultProfile</span></span>
<span data-ttu-id="b4eb3-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4eb3-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="b4eb3-120">-Description</span></span>
<span data-ttu-id="b4eb3-121">Descrição do conjunto de versões da API.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="b4eb3-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="b4eb3-122">-HeaderName</span></span>
<span data-ttu-id="b4eb3-123">O valor de cabeçalho que conterá as informações de controle de versão.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="b4eb3-124">Se o cabeçalho do esquema de controle de versão for escolhido, esse valor deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="b4eb3-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4eb3-125">-Name</span></span>
<span data-ttu-id="b4eb3-126">O nome do conjunto de ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="b4eb3-127">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-127">This parameter is required.</span></span>

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

### <span data-ttu-id="b4eb3-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="b4eb3-128">-QueryName</span></span>
<span data-ttu-id="b4eb3-129">O valor da consulta que conterá as informações de controle de versão.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="b4eb3-130">Se a consulta do esquema de controle de versão for escolhida, esse valor deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-130">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="b4eb3-131">-Esquema</span><span class="sxs-lookup"><span data-stu-id="b4eb3-131">-Scheme</span></span>
<span data-ttu-id="b4eb3-132">Esquema de controle de versão para selecionar para o conjunto de versionamento de API.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="b4eb3-133">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-133">This parameter is required.</span></span>

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

### <span data-ttu-id="b4eb3-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b4eb3-134">-Confirm</span></span>
<span data-ttu-id="b4eb3-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4eb3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4eb3-136">-WhatIf</span></span>
<span data-ttu-id="b4eb3-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4eb3-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4eb3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4eb3-139">CommonParameters</span></span>
<span data-ttu-id="b4eb3-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4eb3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4eb3-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4eb3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4eb3-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4eb3-142">INPUTS</span></span>

### <span data-ttu-id="b4eb3-143">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b4eb3-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="b4eb3-144">Parâmetros: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b4eb3-144">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="b4eb3-145">System. String</span><span class="sxs-lookup"><span data-stu-id="b4eb3-145">System.String</span></span>

### <span data-ttu-id="b4eb3-146">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="b4eb3-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="b4eb3-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4eb3-147">OUTPUTS</span></span>

### <span data-ttu-id="b4eb3-148">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b4eb3-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="b4eb3-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4eb3-149">NOTES</span></span>

## <span data-ttu-id="b4eb3-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4eb3-150">RELATED LINKS</span></span>

[<span data-ttu-id="b4eb3-151">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b4eb3-151">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="b4eb3-152">Remove-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b4eb3-152">Remove-AzureRmApiManagementApiVersionSet</span></span>](./Remove-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="b4eb3-153">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b4eb3-153">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
