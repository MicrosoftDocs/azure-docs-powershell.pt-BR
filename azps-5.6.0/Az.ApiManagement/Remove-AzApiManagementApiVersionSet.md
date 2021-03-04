---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 8f505496bc94d7cd0fc4ca69e6a81324a82871d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891896"
---
# <span data-ttu-id="b4204-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b4204-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="b4204-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4204-102">SYNOPSIS</span></span>
<span data-ttu-id="b4204-103">Remove um conjunto de versão de api específico</span><span class="sxs-lookup"><span data-stu-id="b4204-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="b4204-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b4204-104">SYNTAX</span></span>

### <span data-ttu-id="b4204-105">ExpandedParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b4204-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4204-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b4204-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4204-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4204-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4204-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b4204-108">DESCRIPTION</span></span>

<span data-ttu-id="b4204-109">O cmdlet **Remove-AzAzureRmApiManagementApiVersionSet** remove um Conjunto de Versão da API existente.</span><span class="sxs-lookup"><span data-stu-id="b4204-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="b4204-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4204-110">EXAMPLES</span></span>

### <span data-ttu-id="b4204-111">Exemplo 1: Remover um conjunto de versão da API</span><span class="sxs-lookup"><span data-stu-id="b4204-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="b4204-112">Este comando remove o Conjunto de Versão da API com a ApiVersionSetId especificada.</span><span class="sxs-lookup"><span data-stu-id="b4204-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="b4204-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b4204-113">PARAMETERS</span></span>

### <span data-ttu-id="b4204-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="b4204-114">-ApiVersionSetId</span></span>
<span data-ttu-id="b4204-115">Identificador do Conjunto de Versão da API.</span><span class="sxs-lookup"><span data-stu-id="b4204-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="b4204-116">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b4204-116">This parameter is required.</span></span>

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

### <span data-ttu-id="b4204-117">-Context</span><span class="sxs-lookup"><span data-stu-id="b4204-117">-Context</span></span>
<span data-ttu-id="b4204-118">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b4204-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b4204-119">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b4204-119">This parameter is required.</span></span>

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

### <span data-ttu-id="b4204-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4204-120">-DefaultProfile</span></span>
<span data-ttu-id="b4204-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4204-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4204-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4204-122">-InputObject</span></span>
<span data-ttu-id="b4204-123">Instância de PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="b4204-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="b4204-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b4204-124">This parameter is required.</span></span>

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

### <span data-ttu-id="b4204-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4204-125">-PassThru</span></span>
<span data-ttu-id="b4204-126">Se especificado, a gravação será true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b4204-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b4204-127">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b4204-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="b4204-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4204-128">-ResourceId</span></span>
<span data-ttu-id="b4204-129">Arm ResourceId de ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="b4204-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="b4204-130">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b4204-130">This parameter is required.</span></span>

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

### <span data-ttu-id="b4204-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4204-131">-Confirm</span></span>
<span data-ttu-id="b4204-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4204-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4204-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4204-133">-WhatIf</span></span>
<span data-ttu-id="b4204-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4204-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4204-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4204-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4204-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4204-136">CommonParameters</span></span>
<span data-ttu-id="b4204-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4204-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4204-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4204-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4204-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4204-139">INPUTS</span></span>

### <span data-ttu-id="b4204-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b4204-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b4204-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b4204-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="b4204-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b4204-142">System.String</span></span>

## <span data-ttu-id="b4204-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b4204-143">OUTPUTS</span></span>

### <span data-ttu-id="b4204-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4204-144">System.Boolean</span></span>

## <span data-ttu-id="b4204-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="b4204-145">NOTES</span></span>

## <span data-ttu-id="b4204-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4204-146">RELATED LINKS</span></span>

[<span data-ttu-id="b4204-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b4204-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b4204-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b4204-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b4204-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b4204-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)