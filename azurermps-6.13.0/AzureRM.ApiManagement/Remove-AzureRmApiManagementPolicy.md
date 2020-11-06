---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 1066598a9e255cecbf7238208b5f06f74d88511e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429614"
---
# <span data-ttu-id="19838-101">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="19838-101">Remove-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="19838-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19838-102">SYNOPSIS</span></span>
<span data-ttu-id="19838-103">Remove a política de gerenciamento de API de um escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="19838-103">Removes the API Management policy from a specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19838-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19838-104">SYNTAX</span></span>

### <span data-ttu-id="19838-105">RemoveTenantLevel (padrão)</span><span class="sxs-lookup"><span data-stu-id="19838-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19838-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="19838-106">RemoveProductLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19838-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="19838-107">RemoveApiLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19838-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="19838-108">RemoveOperationLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19838-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19838-109">DESCRIPTION</span></span>
<span data-ttu-id="19838-110">O cmdlet **Remove-AzureRmApiManagementPolicy** remove a política de gerenciamento de API do escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="19838-110">The **Remove-AzureRmApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="19838-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19838-111">EXAMPLES</span></span>

### <span data-ttu-id="19838-112">Exemplo 1: remover a política de nível de locatário</span><span class="sxs-lookup"><span data-stu-id="19838-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="19838-113">Esse comando Remove a política de nível de locatário do gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="19838-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="19838-114">Exemplo 2: remover a política de escopo de produto</span><span class="sxs-lookup"><span data-stu-id="19838-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="19838-115">Esse comando Remove a política de escopo de produto do gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="19838-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="19838-116">Exemplo 3: remover a política de escopo de API</span><span class="sxs-lookup"><span data-stu-id="19838-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="19838-117">Esse comando Remove a política de escopo de API do gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="19838-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="19838-118">Exemplo 4: remover a política de escopo de operação</span><span class="sxs-lookup"><span data-stu-id="19838-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="19838-119">Esse comando Remove a política de escopo de operação do gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="19838-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="19838-120">OS</span><span class="sxs-lookup"><span data-stu-id="19838-120">PARAMETERS</span></span>

### <span data-ttu-id="19838-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="19838-121">-ApiId</span></span>
<span data-ttu-id="19838-122">Especifica o identificador de uma API existente.</span><span class="sxs-lookup"><span data-stu-id="19838-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="19838-123">Se você especificar esse parâmetro, o cmdlet removerá a política de escopo de API.</span><span class="sxs-lookup"><span data-stu-id="19838-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

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

### <span data-ttu-id="19838-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="19838-124">-Context</span></span>
<span data-ttu-id="19838-125">Especifica a instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="19838-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19838-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19838-126">-DefaultProfile</span></span>
<span data-ttu-id="19838-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19838-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19838-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="19838-128">-OperationId</span></span>
<span data-ttu-id="19838-129">Especifica o identificador de uma operação existente.</span><span class="sxs-lookup"><span data-stu-id="19838-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="19838-130">Se você especificar esse parâmetro com o parâmetro *ApiId* , esse cmdlet removerá a política de escopo de operação.</span><span class="sxs-lookup"><span data-stu-id="19838-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

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

### <span data-ttu-id="19838-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19838-131">-PassThru</span></span>
<span data-ttu-id="19838-132">Indica que esse cmdlet retorna um valor de $True, se tiver êxito, ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="19838-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="19838-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="19838-133">-ProductId</span></span>
<span data-ttu-id="19838-134">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="19838-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="19838-135">Se você especificar esse parâmetro, o cmdlet removerá a política de escopo do produto.</span><span class="sxs-lookup"><span data-stu-id="19838-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

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

### <span data-ttu-id="19838-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="19838-136">-Confirm</span></span>
<span data-ttu-id="19838-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19838-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19838-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19838-138">-WhatIf</span></span>
<span data-ttu-id="19838-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="19838-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19838-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="19838-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19838-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19838-141">CommonParameters</span></span>
<span data-ttu-id="19838-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19838-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19838-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19838-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19838-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19838-144">INPUTS</span></span>

### <span data-ttu-id="19838-145">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="19838-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="19838-146">System. String</span><span class="sxs-lookup"><span data-stu-id="19838-146">System.String</span></span>

### <span data-ttu-id="19838-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="19838-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="19838-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19838-148">OUTPUTS</span></span>

### <span data-ttu-id="19838-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19838-149">System.Boolean</span></span>

## <span data-ttu-id="19838-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19838-150">NOTES</span></span>

## <span data-ttu-id="19838-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19838-151">RELATED LINKS</span></span>

[<span data-ttu-id="19838-152">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="19838-152">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="19838-153">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="19838-153">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)

