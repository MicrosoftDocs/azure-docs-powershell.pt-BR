---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 681ce525d1d00802cc226539fd9c3014c1786098
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771392"
---
# <span data-ttu-id="98dbb-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="98dbb-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="98dbb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="98dbb-103">Remove um conjunto de versões de API específico</span><span class="sxs-lookup"><span data-stu-id="98dbb-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="98dbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98dbb-104">SYNTAX</span></span>

### <span data-ttu-id="98dbb-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="98dbb-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98dbb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="98dbb-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98dbb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98dbb-107">DESCRIPTION</span></span>

<span data-ttu-id="98dbb-108">O cmdlet **Remove-AzAzureRmApiManagementApiVersionSet** remove um conjunto de versões de API existente.</span><span class="sxs-lookup"><span data-stu-id="98dbb-108">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="98dbb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98dbb-109">EXAMPLES</span></span>

### <span data-ttu-id="98dbb-110">Exemplo 1: remover um conjunto de versões de API</span><span class="sxs-lookup"><span data-stu-id="98dbb-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="98dbb-111">Esse comando Remove a versão da API definida com o ApiVersionSetId especificado.</span><span class="sxs-lookup"><span data-stu-id="98dbb-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="98dbb-112">OS</span><span class="sxs-lookup"><span data-stu-id="98dbb-112">PARAMETERS</span></span>

### <span data-ttu-id="98dbb-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="98dbb-113">-ApiVersionSetId</span></span>
<span data-ttu-id="98dbb-114">Identificador da versão da API definida.</span><span class="sxs-lookup"><span data-stu-id="98dbb-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="98dbb-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="98dbb-115">This parameter is required.</span></span>

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

### <span data-ttu-id="98dbb-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="98dbb-116">-Context</span></span>
<span data-ttu-id="98dbb-117">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="98dbb-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="98dbb-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="98dbb-118">This parameter is required.</span></span>

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

### <span data-ttu-id="98dbb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98dbb-119">-DefaultProfile</span></span>
<span data-ttu-id="98dbb-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98dbb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98dbb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98dbb-121">-InputObject</span></span>
<span data-ttu-id="98dbb-122">Instância do PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="98dbb-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="98dbb-123">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="98dbb-123">This parameter is required.</span></span>

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

### <span data-ttu-id="98dbb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98dbb-124">-PassThru</span></span>
<span data-ttu-id="98dbb-125">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="98dbb-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="98dbb-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="98dbb-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="98dbb-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="98dbb-127">-Confirm</span></span>
<span data-ttu-id="98dbb-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98dbb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98dbb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98dbb-129">-WhatIf</span></span>
<span data-ttu-id="98dbb-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="98dbb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98dbb-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98dbb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98dbb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98dbb-132">CommonParameters</span></span>
<span data-ttu-id="98dbb-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98dbb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98dbb-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98dbb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98dbb-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98dbb-135">INPUTS</span></span>

### <span data-ttu-id="98dbb-136">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="98dbb-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="98dbb-137">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="98dbb-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="98dbb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="98dbb-138">System.String</span></span>

## <span data-ttu-id="98dbb-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98dbb-139">OUTPUTS</span></span>

### <span data-ttu-id="98dbb-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98dbb-140">System.Boolean</span></span>

## <span data-ttu-id="98dbb-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98dbb-141">NOTES</span></span>

## <span data-ttu-id="98dbb-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98dbb-142">RELATED LINKS</span></span>

[<span data-ttu-id="98dbb-143">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="98dbb-143">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="98dbb-144">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="98dbb-144">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="98dbb-145">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="98dbb-145">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)