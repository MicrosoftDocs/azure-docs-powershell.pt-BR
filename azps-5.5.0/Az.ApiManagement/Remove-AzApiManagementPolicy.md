---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: a51bd7aed5ca8793a921c2cde7729c5280df44b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115553"
---
# <span data-ttu-id="76e4d-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="76e4d-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="76e4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="76e4d-103">Remove a política de Gerenciamento de API de um escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="76e4d-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="76e4d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76e4d-104">SYNTAX</span></span>

### <span data-ttu-id="76e4d-105">RemoveTenantLevel (Padrão)</span><span class="sxs-lookup"><span data-stu-id="76e4d-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76e4d-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="76e4d-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76e4d-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="76e4d-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76e4d-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="76e4d-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76e4d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="76e4d-109">DESCRIPTION</span></span>
<span data-ttu-id="76e4d-110">O cmdlet **Remove-AzApiManagementPolicy** remove a política de Gerenciamento de API do escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="76e4d-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="76e4d-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="76e4d-111">EXAMPLES</span></span>

### <span data-ttu-id="76e4d-112">Exemplo 1: remover a política de nível de locatário</span><span class="sxs-lookup"><span data-stu-id="76e4d-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="76e4d-113">Esse comando remove a política de nível de locatário do Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="76e4d-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="76e4d-114">Exemplo 2: Remover a política de escopo do produto</span><span class="sxs-lookup"><span data-stu-id="76e4d-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="76e4d-115">Esse comando remove a política de escopo do produto do Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="76e4d-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="76e4d-116">Exemplo 3: Remover a política de escopo da API</span><span class="sxs-lookup"><span data-stu-id="76e4d-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="76e4d-117">Esse comando remove a política de escopo da API do Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="76e4d-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="76e4d-118">Exemplo 4: Remover a política de escopo de operação</span><span class="sxs-lookup"><span data-stu-id="76e4d-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="76e4d-119">Esse comando remove a política de escopo de operação do Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="76e4d-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="76e4d-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76e4d-120">PARAMETERS</span></span>

### <span data-ttu-id="76e4d-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="76e4d-121">-ApiId</span></span>
<span data-ttu-id="76e4d-122">Especifica o identificador de uma API existente.</span><span class="sxs-lookup"><span data-stu-id="76e4d-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="76e4d-123">Se você especificar esse parâmetro, o cmdlet removerá a política de escopo da API.</span><span class="sxs-lookup"><span data-stu-id="76e4d-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveApiLevel, RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e4d-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="76e4d-124">-Context</span></span>
<span data-ttu-id="76e4d-125">Especifica a instância do objeto **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="76e4d-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76e4d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76e4d-126">-DefaultProfile</span></span>
<span data-ttu-id="76e4d-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="76e4d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76e4d-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="76e4d-128">-OperationId</span></span>
<span data-ttu-id="76e4d-129">Especifica o identificador de uma operação existente.</span><span class="sxs-lookup"><span data-stu-id="76e4d-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="76e4d-130">Se você especificar esse parâmetro com o parâmetro *ApiId,* esse cmdlet removerá a política de escopo de operação.</span><span class="sxs-lookup"><span data-stu-id="76e4d-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e4d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76e4d-131">-PassThru</span></span>
<span data-ttu-id="76e4d-132">Indica que esse cmdlet retorna um valor de $True, se for bem-sucedido, ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="76e4d-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="76e4d-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="76e4d-133">-ProductId</span></span>
<span data-ttu-id="76e4d-134">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="76e4d-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="76e4d-135">Se você especificar esse parâmetro, o cmdlet removerá a política de escopo do produto.</span><span class="sxs-lookup"><span data-stu-id="76e4d-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e4d-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="76e4d-136">-Confirm</span></span>
<span data-ttu-id="76e4d-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76e4d-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e4d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76e4d-138">-WhatIf</span></span>
<span data-ttu-id="76e4d-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="76e4d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76e4d-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76e4d-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e4d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e4d-141">CommonParameters</span></span>
<span data-ttu-id="76e4d-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76e4d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76e4d-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76e4d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e4d-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="76e4d-144">INPUTS</span></span>

### <span data-ttu-id="76e4d-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="76e4d-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="76e4d-146">System.String</span><span class="sxs-lookup"><span data-stu-id="76e4d-146">System.String</span></span>

### <span data-ttu-id="76e4d-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="76e4d-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="76e4d-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="76e4d-148">OUTPUTS</span></span>

### <span data-ttu-id="76e4d-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="76e4d-149">System.Boolean</span></span>

## <span data-ttu-id="76e4d-150">Notas</span><span class="sxs-lookup"><span data-stu-id="76e4d-150">NOTES</span></span>

## <span data-ttu-id="76e4d-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76e4d-151">RELATED LINKS</span></span>

[<span data-ttu-id="76e4d-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="76e4d-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="76e4d-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="76e4d-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


