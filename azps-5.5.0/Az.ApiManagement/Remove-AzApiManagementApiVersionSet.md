---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58a082288a121e5e6b04353bad862edaea4c20fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127167"
---
# <span data-ttu-id="05329-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="05329-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="05329-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05329-102">SYNOPSIS</span></span>
<span data-ttu-id="05329-103">Remove um determinado Conjunto de Versões da Api</span><span class="sxs-lookup"><span data-stu-id="05329-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="05329-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05329-104">SYNTAX</span></span>

### <span data-ttu-id="05329-105">ExpandedParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="05329-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05329-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="05329-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05329-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="05329-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05329-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="05329-108">DESCRIPTION</span></span>

<span data-ttu-id="05329-109">O cmdlet **Remove-AzAzureRmApiManagementApiVersionSet** remove um conjunto de versões da API existente.</span><span class="sxs-lookup"><span data-stu-id="05329-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="05329-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="05329-110">EXAMPLES</span></span>

### <span data-ttu-id="05329-111">Exemplo 1: Remover um conjunto de versões da API</span><span class="sxs-lookup"><span data-stu-id="05329-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="05329-112">Esse comando remove o Conjunto de Versões da API com o ApiVersionSetId especificado.</span><span class="sxs-lookup"><span data-stu-id="05329-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="05329-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05329-113">PARAMETERS</span></span>

### <span data-ttu-id="05329-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="05329-114">-ApiVersionSetId</span></span>
<span data-ttu-id="05329-115">Identificador do Conjunto de Versões da API.</span><span class="sxs-lookup"><span data-stu-id="05329-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="05329-116">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="05329-116">This parameter is required.</span></span>

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

### <span data-ttu-id="05329-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="05329-117">-Context</span></span>
<span data-ttu-id="05329-118">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="05329-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="05329-119">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="05329-119">This parameter is required.</span></span>

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

### <span data-ttu-id="05329-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05329-120">-DefaultProfile</span></span>
<span data-ttu-id="05329-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05329-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05329-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05329-122">-InputObject</span></span>
<span data-ttu-id="05329-123">Instância do PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="05329-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="05329-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="05329-124">This parameter is required.</span></span>

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

### <span data-ttu-id="05329-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05329-125">-PassThru</span></span>
<span data-ttu-id="05329-126">Se especificado, a gravação será verdadeira caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="05329-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="05329-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="05329-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="05329-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05329-128">-ResourceId</span></span>
<span data-ttu-id="05329-129">Arm ResourceId do ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="05329-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="05329-130">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="05329-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05329-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="05329-131">-Confirm</span></span>
<span data-ttu-id="05329-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05329-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05329-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05329-133">-WhatIf</span></span>
<span data-ttu-id="05329-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="05329-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05329-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05329-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05329-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05329-136">CommonParameters</span></span>
<span data-ttu-id="05329-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05329-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05329-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05329-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05329-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="05329-139">INPUTS</span></span>

### <span data-ttu-id="05329-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="05329-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="05329-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="05329-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="05329-142">System.String</span><span class="sxs-lookup"><span data-stu-id="05329-142">System.String</span></span>

## <span data-ttu-id="05329-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="05329-143">OUTPUTS</span></span>

### <span data-ttu-id="05329-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="05329-144">System.Boolean</span></span>

## <span data-ttu-id="05329-145">Notas</span><span class="sxs-lookup"><span data-stu-id="05329-145">NOTES</span></span>

## <span data-ttu-id="05329-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05329-146">RELATED LINKS</span></span>

[<span data-ttu-id="05329-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="05329-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="05329-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="05329-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="05329-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="05329-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)