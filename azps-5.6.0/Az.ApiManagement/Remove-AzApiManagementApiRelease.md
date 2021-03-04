---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 3759b5255794fcceb16018ecfc49bba362a03928
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893258"
---
# <span data-ttu-id="c970d-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c970d-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="c970d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c970d-102">SYNOPSIS</span></span>
<span data-ttu-id="c970d-103">Remove uma versão específica da API</span><span class="sxs-lookup"><span data-stu-id="c970d-103">Removes a particular API Release</span></span>

## <span data-ttu-id="c970d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c970d-104">SYNTAX</span></span>

### <span data-ttu-id="c970d-105">ByApiReleaseId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c970d-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c970d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c970d-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c970d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c970d-107">DESCRIPTION</span></span>

<span data-ttu-id="c970d-108">O cmdlet **Remove-AzAzureRmApiManagementApiRelease** remove uma versão da API existente.</span><span class="sxs-lookup"><span data-stu-id="c970d-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="c970d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c970d-109">EXAMPLES</span></span>

### <span data-ttu-id="c970d-110">Exemplo 1: Remover uma versão da API</span><span class="sxs-lookup"><span data-stu-id="c970d-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="c970d-111">Este comando remove a Versão da API com as ApiId e ReleaseId especificadas.</span><span class="sxs-lookup"><span data-stu-id="c970d-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="c970d-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c970d-112">PARAMETERS</span></span>

### <span data-ttu-id="c970d-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c970d-113">-ApiId</span></span>
<span data-ttu-id="c970d-114">Identificador da API.</span><span class="sxs-lookup"><span data-stu-id="c970d-114">Identifier of the API.</span></span>
<span data-ttu-id="c970d-115">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c970d-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c970d-116">-Context</span><span class="sxs-lookup"><span data-stu-id="c970d-116">-Context</span></span>
<span data-ttu-id="c970d-117">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c970d-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c970d-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c970d-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c970d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c970d-119">-DefaultProfile</span></span>
<span data-ttu-id="c970d-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c970d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c970d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c970d-121">-InputObject</span></span>
<span data-ttu-id="c970d-122">Instância de PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="c970d-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="c970d-123">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c970d-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c970d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c970d-124">-PassThru</span></span>
<span data-ttu-id="c970d-125">Se especificado, a gravação será true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c970d-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c970d-126">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c970d-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="c970d-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="c970d-127">-ReleaseId</span></span>
<span data-ttu-id="c970d-128">Identificador da Versão da API.</span><span class="sxs-lookup"><span data-stu-id="c970d-128">Identifier of the API Release.</span></span>
<span data-ttu-id="c970d-129">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c970d-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c970d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c970d-130">-Confirm</span></span>
<span data-ttu-id="c970d-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c970d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c970d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c970d-132">-WhatIf</span></span>
<span data-ttu-id="c970d-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c970d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c970d-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c970d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c970d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c970d-135">CommonParameters</span></span>
<span data-ttu-id="c970d-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c970d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c970d-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c970d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c970d-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c970d-138">INPUTS</span></span>

### <span data-ttu-id="c970d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c970d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c970d-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c970d-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="c970d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c970d-141">System.String</span></span>

## <span data-ttu-id="c970d-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c970d-142">OUTPUTS</span></span>

### <span data-ttu-id="c970d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c970d-143">System.Boolean</span></span>

## <span data-ttu-id="c970d-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="c970d-144">NOTES</span></span>

## <span data-ttu-id="c970d-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c970d-145">RELATED LINKS</span></span>

[<span data-ttu-id="c970d-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c970d-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="c970d-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c970d-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="c970d-148">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c970d-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)