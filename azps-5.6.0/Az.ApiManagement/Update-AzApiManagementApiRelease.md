---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 16c73a389e6602999272255534312928fc4a13f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888753"
---
# <span data-ttu-id="16729-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="16729-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="16729-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16729-102">SYNOPSIS</span></span>
<span data-ttu-id="16729-103">Atualiza um determinado Lançamento de Api.</span><span class="sxs-lookup"><span data-stu-id="16729-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="16729-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="16729-104">SYNTAX</span></span>

### <span data-ttu-id="16729-105">ExpandedParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="16729-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16729-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="16729-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16729-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="16729-107">DESCRIPTION</span></span>
<span data-ttu-id="16729-108">O cmdlet **Update-AzApiManagementApiRelease** modifica um Lançamento da API de Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="16729-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="16729-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16729-109">EXAMPLES</span></span>

### <span data-ttu-id="16729-110">Exemplo 1: atualiza uma versão da API para uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="16729-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="16729-111">Este comando atualiza a `echo-api-release` Versão da API da Api com nova `echo-api` nota.</span><span class="sxs-lookup"><span data-stu-id="16729-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="16729-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="16729-112">PARAMETERS</span></span>

### <span data-ttu-id="16729-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="16729-113">-ApiId</span></span>
<span data-ttu-id="16729-114">Identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="16729-114">Identifier of existing API.</span></span>
<span data-ttu-id="16729-115">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="16729-115">This parameter is required.</span></span>

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

### <span data-ttu-id="16729-116">-Context</span><span class="sxs-lookup"><span data-stu-id="16729-116">-Context</span></span>
<span data-ttu-id="16729-117">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="16729-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="16729-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="16729-118">This parameter is required.</span></span>

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

### <span data-ttu-id="16729-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16729-119">-DefaultProfile</span></span>
<span data-ttu-id="16729-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16729-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16729-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16729-121">-InputObject</span></span>
<span data-ttu-id="16729-122">Instância do tipo Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="16729-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

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

### <span data-ttu-id="16729-123">-Observação</span><span class="sxs-lookup"><span data-stu-id="16729-123">-Note</span></span>
<span data-ttu-id="16729-124">Notas de versão da api.</span><span class="sxs-lookup"><span data-stu-id="16729-124">Api Release Notes.</span></span>
<span data-ttu-id="16729-125">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="16729-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="16729-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16729-126">-PassThru</span></span>
<span data-ttu-id="16729-127">Se especificado, em seguida, instância do tipo Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease que representa a versão definida da API.</span><span class="sxs-lookup"><span data-stu-id="16729-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="16729-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="16729-128">-ReleaseId</span></span>
<span data-ttu-id="16729-129">Identificador do ReleaseId de Revisão da Api.</span><span class="sxs-lookup"><span data-stu-id="16729-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="16729-130">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="16729-130">This parameter is required.</span></span>

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

### <span data-ttu-id="16729-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16729-131">-Confirm</span></span>
<span data-ttu-id="16729-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16729-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16729-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16729-133">-WhatIf</span></span>
<span data-ttu-id="16729-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="16729-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16729-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16729-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16729-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16729-136">CommonParameters</span></span>
<span data-ttu-id="16729-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16729-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16729-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16729-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16729-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16729-139">INPUTS</span></span>

### <span data-ttu-id="16729-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="16729-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="16729-141">System.String</span><span class="sxs-lookup"><span data-stu-id="16729-141">System.String</span></span>

### <span data-ttu-id="16729-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="16729-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="16729-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="16729-143">OUTPUTS</span></span>

### <span data-ttu-id="16729-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="16729-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="16729-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="16729-145">NOTES</span></span>

## <span data-ttu-id="16729-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16729-146">RELATED LINKS</span></span>

[<span data-ttu-id="16729-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="16729-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="16729-148">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="16729-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
