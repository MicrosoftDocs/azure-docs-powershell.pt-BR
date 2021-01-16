---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58a082288a121e5e6b04353bad862edaea4c20fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272174"
---
# <span data-ttu-id="1e435-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1e435-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1e435-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e435-102">SYNOPSIS</span></span>
<span data-ttu-id="1e435-103">Remove um conjunto de versões de API específico</span><span class="sxs-lookup"><span data-stu-id="1e435-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="1e435-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e435-104">SYNTAX</span></span>

### <span data-ttu-id="1e435-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="1e435-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e435-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1e435-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e435-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1e435-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e435-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e435-108">DESCRIPTION</span></span>

<span data-ttu-id="1e435-109">O cmdlet **Remove-AzAzureRmApiManagementApiVersionSet** remove um conjunto de versões de API existente.</span><span class="sxs-lookup"><span data-stu-id="1e435-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="1e435-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e435-110">EXAMPLES</span></span>

### <span data-ttu-id="1e435-111">Exemplo 1: remover um conjunto de versões de API</span><span class="sxs-lookup"><span data-stu-id="1e435-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="1e435-112">Esse comando Remove a versão da API definida com o ApiVersionSetId especificado.</span><span class="sxs-lookup"><span data-stu-id="1e435-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="1e435-113">OS</span><span class="sxs-lookup"><span data-stu-id="1e435-113">PARAMETERS</span></span>

### <span data-ttu-id="1e435-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="1e435-114">-ApiVersionSetId</span></span>
<span data-ttu-id="1e435-115">Identificador da versão da API definida.</span><span class="sxs-lookup"><span data-stu-id="1e435-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="1e435-116">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1e435-116">This parameter is required.</span></span>

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

### <span data-ttu-id="1e435-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1e435-117">-Context</span></span>
<span data-ttu-id="1e435-118">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1e435-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1e435-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1e435-119">This parameter is required.</span></span>

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

### <span data-ttu-id="1e435-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e435-120">-DefaultProfile</span></span>
<span data-ttu-id="1e435-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1e435-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e435-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e435-122">-InputObject</span></span>
<span data-ttu-id="1e435-123">Instância do PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="1e435-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="1e435-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1e435-124">This parameter is required.</span></span>

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

### <span data-ttu-id="1e435-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e435-125">-PassThru</span></span>
<span data-ttu-id="1e435-126">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1e435-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="1e435-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="1e435-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="1e435-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e435-128">-ResourceId</span></span>
<span data-ttu-id="1e435-129">Resourcebinding de ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="1e435-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="1e435-130">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1e435-130">This parameter is required.</span></span>

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

### <span data-ttu-id="1e435-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1e435-131">-Confirm</span></span>
<span data-ttu-id="1e435-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e435-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e435-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e435-133">-WhatIf</span></span>
<span data-ttu-id="1e435-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e435-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e435-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e435-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e435-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e435-136">CommonParameters</span></span>
<span data-ttu-id="1e435-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e435-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e435-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e435-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e435-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e435-139">INPUTS</span></span>

### <span data-ttu-id="1e435-140">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1e435-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1e435-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1e435-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="1e435-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1e435-142">System.String</span></span>

## <span data-ttu-id="1e435-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e435-143">OUTPUTS</span></span>

### <span data-ttu-id="1e435-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e435-144">System.Boolean</span></span>

## <span data-ttu-id="1e435-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e435-145">NOTES</span></span>

## <span data-ttu-id="1e435-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e435-146">RELATED LINKS</span></span>

[<span data-ttu-id="1e435-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1e435-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="1e435-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1e435-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="1e435-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1e435-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)