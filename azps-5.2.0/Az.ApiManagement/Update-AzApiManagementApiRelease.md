---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 99ec1234eea582fb91f2722032cb23c27e86b878
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260667"
---
# <span data-ttu-id="2573c-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="2573c-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="2573c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2573c-102">SYNOPSIS</span></span>
<span data-ttu-id="2573c-103">Atualiza uma versão de API específica.</span><span class="sxs-lookup"><span data-stu-id="2573c-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="2573c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2573c-104">SYNTAX</span></span>

### <span data-ttu-id="2573c-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="2573c-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2573c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2573c-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2573c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2573c-107">DESCRIPTION</span></span>
<span data-ttu-id="2573c-108">O cmdlet **Update-AzApiManagementApiRelease** modifica uma versão da API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="2573c-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="2573c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2573c-109">EXAMPLES</span></span>

### <span data-ttu-id="2573c-110">Exemplo 1: atualiza uma versão de API para uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="2573c-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="2573c-111">Esse comando atualiza a `echo-api-release` versão da API da API `echo-api` com uma nova anotação.</span><span class="sxs-lookup"><span data-stu-id="2573c-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="2573c-112">OS</span><span class="sxs-lookup"><span data-stu-id="2573c-112">PARAMETERS</span></span>

### <span data-ttu-id="2573c-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2573c-113">-ApiId</span></span>
<span data-ttu-id="2573c-114">Identificador de API existente.</span><span class="sxs-lookup"><span data-stu-id="2573c-114">Identifier of existing API.</span></span>
<span data-ttu-id="2573c-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2573c-115">This parameter is required.</span></span>

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

### <span data-ttu-id="2573c-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2573c-116">-Context</span></span>
<span data-ttu-id="2573c-117">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2573c-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2573c-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2573c-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2573c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2573c-119">-DefaultProfile</span></span>
<span data-ttu-id="2573c-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2573c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2573c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2573c-121">-InputObject</span></span>
<span data-ttu-id="2573c-122">Instância do tipo Microsoft. Azure. Commands. ApiManagement. inmanagement. Models. PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="2573c-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2573c-123">-Nota</span><span class="sxs-lookup"><span data-stu-id="2573c-123">-Note</span></span>
<span data-ttu-id="2573c-124">Notas de versão da API.</span><span class="sxs-lookup"><span data-stu-id="2573c-124">Api Release Notes.</span></span>
<span data-ttu-id="2573c-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="2573c-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="2573c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2573c-126">-PassThru</span></span>
<span data-ttu-id="2573c-127">Se especificado, a instância do tipo Microsoft. Azure. Commands. ApiManagement. PsApiManagementApiRelease. Models. que representa a versão da API Set.</span><span class="sxs-lookup"><span data-stu-id="2573c-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="2573c-128">-Rereleaseid</span><span class="sxs-lookup"><span data-stu-id="2573c-128">-ReleaseId</span></span>
<span data-ttu-id="2573c-129">Identificador para a revisão de API releaseid.</span><span class="sxs-lookup"><span data-stu-id="2573c-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="2573c-130">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2573c-130">This parameter is required.</span></span>

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

### <span data-ttu-id="2573c-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2573c-131">-Confirm</span></span>
<span data-ttu-id="2573c-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2573c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2573c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2573c-133">-WhatIf</span></span>
<span data-ttu-id="2573c-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2573c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2573c-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2573c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2573c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2573c-136">CommonParameters</span></span>
<span data-ttu-id="2573c-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2573c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2573c-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2573c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2573c-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2573c-139">INPUTS</span></span>

### <span data-ttu-id="2573c-140">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2573c-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2573c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2573c-141">System.String</span></span>

### <span data-ttu-id="2573c-142">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="2573c-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="2573c-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2573c-143">OUTPUTS</span></span>

### <span data-ttu-id="2573c-144">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="2573c-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="2573c-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2573c-145">NOTES</span></span>

## <span data-ttu-id="2573c-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2573c-146">RELATED LINKS</span></span>

[<span data-ttu-id="2573c-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="2573c-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="2573c-148">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="2573c-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
