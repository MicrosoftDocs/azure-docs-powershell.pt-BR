---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 99ec1234eea582fb91f2722032cb23c27e86b878
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116641"
---
# <span data-ttu-id="d7b8a-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d7b8a-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="d7b8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7b8a-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b8a-103">Atualiza um lançamento de Api específico.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="d7b8a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7b8a-104">SYNTAX</span></span>

### <span data-ttu-id="d7b8a-105">ExpandedParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d7b8a-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7b8a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d7b8a-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7b8a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7b8a-107">DESCRIPTION</span></span>
<span data-ttu-id="d7b8a-108">O cmdlet **Update-AzApiManagementApiRelease** modifica uma versão da API de gerenciamento da API do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="d7b8a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d7b8a-109">EXAMPLES</span></span>

### <span data-ttu-id="d7b8a-110">Exemplo 1: atualiza uma versão da API para uma revisão da API</span><span class="sxs-lookup"><span data-stu-id="d7b8a-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="d7b8a-111">Este comando atualiza o `echo-api-release` Lançamento da API da Api com uma nova `echo-api` anotação.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="d7b8a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7b8a-112">PARAMETERS</span></span>

### <span data-ttu-id="d7b8a-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d7b8a-113">-ApiId</span></span>
<span data-ttu-id="d7b8a-114">Identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-114">Identifier of existing API.</span></span>
<span data-ttu-id="d7b8a-115">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-115">This parameter is required.</span></span>

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

### <span data-ttu-id="d7b8a-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d7b8a-116">-Context</span></span>
<span data-ttu-id="d7b8a-117">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d7b8a-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-118">This parameter is required.</span></span>

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

### <span data-ttu-id="d7b8a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b8a-119">-DefaultProfile</span></span>
<span data-ttu-id="d7b8a-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7b8a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7b8a-121">-InputObject</span></span>
<span data-ttu-id="d7b8a-122">Instância do tipo Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

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

### <span data-ttu-id="d7b8a-123">-Observação</span><span class="sxs-lookup"><span data-stu-id="d7b8a-123">-Note</span></span>
<span data-ttu-id="d7b8a-124">Notas de Versão da Api.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-124">Api Release Notes.</span></span>
<span data-ttu-id="d7b8a-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="d7b8a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7b8a-126">-PassThru</span></span>
<span data-ttu-id="d7b8a-127">Se especificado, então instância do tipo Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease que representa o lançamento de API definido.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="d7b8a-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="d7b8a-128">-ReleaseId</span></span>
<span data-ttu-id="d7b8a-129">Identificador do ReleaseId de Revisão da Api.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="d7b8a-130">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-130">This parameter is required.</span></span>

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

### <span data-ttu-id="d7b8a-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d7b8a-131">-Confirm</span></span>
<span data-ttu-id="d7b8a-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7b8a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7b8a-133">-WhatIf</span></span>
<span data-ttu-id="d7b8a-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7b8a-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7b8a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b8a-136">CommonParameters</span></span>
<span data-ttu-id="d7b8a-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7b8a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b8a-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7b8a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b8a-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="d7b8a-139">INPUTS</span></span>

### <span data-ttu-id="d7b8a-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d7b8a-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d7b8a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d7b8a-141">System.String</span></span>

### <span data-ttu-id="d7b8a-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d7b8a-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="d7b8a-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="d7b8a-143">OUTPUTS</span></span>

### <span data-ttu-id="d7b8a-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d7b8a-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="d7b8a-145">Notas</span><span class="sxs-lookup"><span data-stu-id="d7b8a-145">NOTES</span></span>

## <span data-ttu-id="d7b8a-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7b8a-146">RELATED LINKS</span></span>

[<span data-ttu-id="d7b8a-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d7b8a-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="d7b8a-148">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d7b8a-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
