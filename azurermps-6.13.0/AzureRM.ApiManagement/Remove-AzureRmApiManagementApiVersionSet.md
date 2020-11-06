---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 4ff48709b02cdd0270c559ea8be2f4e269dbce2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93601994"
---
# <span data-ttu-id="6c90e-101">Remove-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6c90e-101">Remove-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="6c90e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c90e-102">SYNOPSIS</span></span>
<span data-ttu-id="6c90e-103">Remove um conjunto de versões de API específico</span><span class="sxs-lookup"><span data-stu-id="6c90e-103">Removes a particular Api Version Set</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c90e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c90e-104">SYNTAX</span></span>

### <span data-ttu-id="6c90e-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="6c90e-105">ExpandedParameter (Default)</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c90e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6c90e-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c90e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c90e-107">DESCRIPTION</span></span>

<span data-ttu-id="6c90e-108">O cmdlet **Remove-AzureRmApiManagementApiVersionSet** remove um conjunto de versões de API existente.</span><span class="sxs-lookup"><span data-stu-id="6c90e-108">The **Remove-AzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="6c90e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c90e-109">EXAMPLES</span></span>

### <span data-ttu-id="6c90e-110">Exemplo 1: remover um conjunto de versões de API</span><span class="sxs-lookup"><span data-stu-id="6c90e-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="6c90e-111">Esse comando Remove a versão da API definida com o ApiVersionSetId especificado.</span><span class="sxs-lookup"><span data-stu-id="6c90e-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="6c90e-112">OS</span><span class="sxs-lookup"><span data-stu-id="6c90e-112">PARAMETERS</span></span>

### <span data-ttu-id="6c90e-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="6c90e-113">-ApiVersionSetId</span></span>
<span data-ttu-id="6c90e-114">Identificador da versão da API definida.</span><span class="sxs-lookup"><span data-stu-id="6c90e-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="6c90e-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6c90e-115">This parameter is required.</span></span>

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

### <span data-ttu-id="6c90e-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="6c90e-116">-Context</span></span>
<span data-ttu-id="6c90e-117">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6c90e-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6c90e-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6c90e-118">This parameter is required.</span></span>

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

### <span data-ttu-id="6c90e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c90e-119">-DefaultProfile</span></span>
<span data-ttu-id="6c90e-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6c90e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c90e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c90e-121">-InputObject</span></span>
<span data-ttu-id="6c90e-122">Instância do PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="6c90e-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="6c90e-123">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6c90e-123">This parameter is required.</span></span>

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

### <span data-ttu-id="6c90e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c90e-124">-PassThru</span></span>
<span data-ttu-id="6c90e-125">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6c90e-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="6c90e-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="6c90e-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="6c90e-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6c90e-127">-Confirm</span></span>
<span data-ttu-id="6c90e-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c90e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c90e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c90e-129">-WhatIf</span></span>
<span data-ttu-id="6c90e-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6c90e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c90e-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6c90e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c90e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c90e-132">CommonParameters</span></span>
<span data-ttu-id="6c90e-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c90e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c90e-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c90e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c90e-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c90e-135">INPUTS</span></span>

### <span data-ttu-id="6c90e-136">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6c90e-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="6c90e-137">Parâmetros: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6c90e-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="6c90e-138">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6c90e-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="6c90e-139">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6c90e-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="6c90e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6c90e-140">System.String</span></span>

## <span data-ttu-id="6c90e-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c90e-141">OUTPUTS</span></span>

### <span data-ttu-id="6c90e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c90e-142">System.Boolean</span></span>

## <span data-ttu-id="6c90e-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c90e-143">NOTES</span></span>

## <span data-ttu-id="6c90e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c90e-144">RELATED LINKS</span></span>

[<span data-ttu-id="6c90e-145">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6c90e-145">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="6c90e-146">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6c90e-146">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="6c90e-147">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6c90e-147">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
