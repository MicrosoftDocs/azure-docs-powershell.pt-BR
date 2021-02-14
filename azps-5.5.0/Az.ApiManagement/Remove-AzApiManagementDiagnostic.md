---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 488f4082007c96a111483d7efac6a8b9a74dba8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111230"
---
# <span data-ttu-id="4d368-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4d368-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="4d368-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d368-102">SYNOPSIS</span></span>
<span data-ttu-id="4d368-103">Remova a entidade diagnóstico do escopo de nível Global ou API.</span><span class="sxs-lookup"><span data-stu-id="4d368-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="4d368-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d368-104">SYNTAX</span></span>

### <span data-ttu-id="4d368-105">ByResourceIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4d368-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d368-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="4d368-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d368-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d368-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d368-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d368-108">DESCRIPTION</span></span>
<span data-ttu-id="4d368-109">O cmdlet **Remove-AzApiManagementDiagnostic** remove a entidade de diagnóstico especificada pelo escopo global ou `DiagnosticId` por um `ApiId` escopo</span><span class="sxs-lookup"><span data-stu-id="4d368-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="4d368-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4d368-110">EXAMPLES</span></span>

### <span data-ttu-id="4d368-111">Exemplo 1: Remover a entidade diagnóstico</span><span class="sxs-lookup"><span data-stu-id="4d368-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="4d368-112">Este exemplo remove o diagnóstico `applicationinsights` do serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="4d368-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="4d368-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d368-113">PARAMETERS</span></span>

### <span data-ttu-id="4d368-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4d368-114">-ApiId</span></span>
<span data-ttu-id="4d368-115">Identificador da API.</span><span class="sxs-lookup"><span data-stu-id="4d368-115">Identifier of the API.</span></span>
<span data-ttu-id="4d368-116">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="4d368-116">This parameter is required.</span></span>

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

### <span data-ttu-id="4d368-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="4d368-117">-Context</span></span>
<span data-ttu-id="4d368-118">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4d368-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4d368-119">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="4d368-119">This parameter is required.</span></span>

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

### <span data-ttu-id="4d368-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d368-120">-DefaultProfile</span></span>
<span data-ttu-id="4d368-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d368-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d368-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="4d368-122">-DiagnosticId</span></span>
<span data-ttu-id="4d368-123">Identificador de produto existente.</span><span class="sxs-lookup"><span data-stu-id="4d368-123">Identifier of existing product.</span></span>
<span data-ttu-id="4d368-124">Se especificado, retornará a política de escopo do produto.</span><span class="sxs-lookup"><span data-stu-id="4d368-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="4d368-125">Esses parâmetros são opcionais.</span><span class="sxs-lookup"><span data-stu-id="4d368-125">This parameters is optional.</span></span>

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

### <span data-ttu-id="4d368-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d368-126">-InputObject</span></span>
<span data-ttu-id="4d368-127">Instância de PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="4d368-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="4d368-128">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="4d368-128">This parameter is required.</span></span>

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

### <span data-ttu-id="4d368-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d368-129">-PassThru</span></span>
<span data-ttu-id="4d368-130">Se especificado, a gravação será verdadeira caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4d368-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="4d368-131">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="4d368-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="4d368-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d368-132">-ResourceId</span></span>
<span data-ttu-id="4d368-133">Arm ResourceId of Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="4d368-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="4d368-134">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="4d368-134">This parameter is required.</span></span>

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

### <span data-ttu-id="4d368-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4d368-135">-Confirm</span></span>
<span data-ttu-id="4d368-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d368-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d368-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d368-137">-WhatIf</span></span>
<span data-ttu-id="4d368-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4d368-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d368-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d368-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d368-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d368-140">CommonParameters</span></span>
<span data-ttu-id="4d368-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d368-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d368-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d368-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d368-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="4d368-143">INPUTS</span></span>

### <span data-ttu-id="4d368-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4d368-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4d368-145">System.String</span><span class="sxs-lookup"><span data-stu-id="4d368-145">System.String</span></span>

### <span data-ttu-id="4d368-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4d368-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4d368-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="4d368-147">OUTPUTS</span></span>

### <span data-ttu-id="4d368-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d368-148">System.Boolean</span></span>

## <span data-ttu-id="4d368-149">Notas</span><span class="sxs-lookup"><span data-stu-id="4d368-149">NOTES</span></span>

## <span data-ttu-id="4d368-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d368-150">RELATED LINKS</span></span>

[<span data-ttu-id="4d368-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4d368-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="4d368-152">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4d368-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="4d368-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4d368-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)