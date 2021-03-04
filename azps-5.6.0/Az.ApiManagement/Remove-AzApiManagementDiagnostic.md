---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 4f6f7f1cf2223d4ef139d60e710f4a861149a3ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901369"
---
# <span data-ttu-id="caab2-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="caab2-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="caab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caab2-102">SYNOPSIS</span></span>
<span data-ttu-id="caab2-103">Remova a entidade Diagnostic do escopo global ou de nível de API.</span><span class="sxs-lookup"><span data-stu-id="caab2-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="caab2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="caab2-104">SYNTAX</span></span>

### <span data-ttu-id="caab2-105">ByResourceIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="caab2-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caab2-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="caab2-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caab2-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="caab2-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caab2-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="caab2-108">DESCRIPTION</span></span>
<span data-ttu-id="caab2-109">O cmdlet **Remove-AzApiManagementDiagnostic** remove a entidade de diagnóstico especificada pelo escopo global ou `DiagnosticId` por um `ApiId` escopo</span><span class="sxs-lookup"><span data-stu-id="caab2-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="caab2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="caab2-110">EXAMPLES</span></span>

### <span data-ttu-id="caab2-111">Exemplo 1: Remover a entidade Diagnostic</span><span class="sxs-lookup"><span data-stu-id="caab2-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="caab2-112">Este exemplo remove o diagnóstico `applicationinsights` do serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="caab2-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="caab2-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="caab2-113">PARAMETERS</span></span>

### <span data-ttu-id="caab2-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="caab2-114">-ApiId</span></span>
<span data-ttu-id="caab2-115">Identificador da API.</span><span class="sxs-lookup"><span data-stu-id="caab2-115">Identifier of the API.</span></span>
<span data-ttu-id="caab2-116">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="caab2-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caab2-117">-Context</span><span class="sxs-lookup"><span data-stu-id="caab2-117">-Context</span></span>
<span data-ttu-id="caab2-118">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="caab2-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="caab2-119">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="caab2-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="caab2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caab2-120">-DefaultProfile</span></span>
<span data-ttu-id="caab2-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="caab2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caab2-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="caab2-122">-DiagnosticId</span></span>
<span data-ttu-id="caab2-123">Identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="caab2-123">Identifier of existing product.</span></span>
<span data-ttu-id="caab2-124">Se especificado, retornará a política de escopo do produto.</span><span class="sxs-lookup"><span data-stu-id="caab2-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="caab2-125">Esses parâmetros são opcionais.</span><span class="sxs-lookup"><span data-stu-id="caab2-125">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caab2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="caab2-126">-InputObject</span></span>
<span data-ttu-id="caab2-127">Instância de PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="caab2-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="caab2-128">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="caab2-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="caab2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="caab2-129">-PassThru</span></span>
<span data-ttu-id="caab2-130">Se especificado, a gravação será true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="caab2-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="caab2-131">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="caab2-131">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caab2-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="caab2-132">-ResourceId</span></span>
<span data-ttu-id="caab2-133">Arm ResourceId de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="caab2-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="caab2-134">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="caab2-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caab2-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="caab2-135">-Confirm</span></span>
<span data-ttu-id="caab2-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="caab2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caab2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caab2-137">-WhatIf</span></span>
<span data-ttu-id="caab2-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="caab2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caab2-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="caab2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caab2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caab2-140">CommonParameters</span></span>
<span data-ttu-id="caab2-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caab2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caab2-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="caab2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caab2-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="caab2-143">INPUTS</span></span>

### <span data-ttu-id="caab2-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="caab2-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="caab2-145">System.String</span><span class="sxs-lookup"><span data-stu-id="caab2-145">System.String</span></span>

### <span data-ttu-id="caab2-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="caab2-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="caab2-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="caab2-147">OUTPUTS</span></span>

### <span data-ttu-id="caab2-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="caab2-148">System.Boolean</span></span>

## <span data-ttu-id="caab2-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="caab2-149">NOTES</span></span>

## <span data-ttu-id="caab2-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="caab2-150">RELATED LINKS</span></span>

[<span data-ttu-id="caab2-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="caab2-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="caab2-152">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="caab2-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="caab2-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="caab2-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)