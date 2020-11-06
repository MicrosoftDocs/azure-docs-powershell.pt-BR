---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 5f7fa78cb368afe3e277661122682f43f885f7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427031"
---
# <span data-ttu-id="5ad18-101">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5ad18-101">Remove-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="5ad18-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ad18-102">SYNOPSIS</span></span>
<span data-ttu-id="5ad18-103">Remove a política de gerenciamento de API de um escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="5ad18-103">Removes the API Management policy from a specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ad18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ad18-104">SYNTAX</span></span>

### <span data-ttu-id="5ad18-105">Nível do locatário (padrão)</span><span class="sxs-lookup"><span data-stu-id="5ad18-105">Tenant level (Default)</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ad18-106">Nível do produto</span><span class="sxs-lookup"><span data-stu-id="5ad18-106">Product level</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ad18-107">Nível de API</span><span class="sxs-lookup"><span data-stu-id="5ad18-107">API level</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ad18-108">Nível de operação</span><span class="sxs-lookup"><span data-stu-id="5ad18-108">Operation level</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ad18-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ad18-109">DESCRIPTION</span></span>
<span data-ttu-id="5ad18-110">O cmdlet **Remove-AzureRmApiManagementPolicy** remove a política de gerenciamento de API do escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="5ad18-110">The **Remove-AzureRmApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="5ad18-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ad18-111">EXAMPLES</span></span>

### <span data-ttu-id="5ad18-112">Exemplo 1: remover a política de nível de locatário</span><span class="sxs-lookup"><span data-stu-id="5ad18-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext
```

<span data-ttu-id="5ad18-113">Esse comando Remove a política de nível de locatário do gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="5ad18-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="5ad18-114">Exemplo 2: remover a política de escopo de produto</span><span class="sxs-lookup"><span data-stu-id="5ad18-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="5ad18-115">Esse comando Remove a política de escopo de produto do gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="5ad18-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="5ad18-116">Exemplo 3: remover a política de escopo de API</span><span class="sxs-lookup"><span data-stu-id="5ad18-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

<span data-ttu-id="5ad18-117">Esse comando Remove a política de escopo de API do gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="5ad18-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="5ad18-118">Exemplo 4: remover a política de escopo de operação</span><span class="sxs-lookup"><span data-stu-id="5ad18-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="5ad18-119">Esse comando Remove a política de escopo de operação do gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="5ad18-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="5ad18-120">OS</span><span class="sxs-lookup"><span data-stu-id="5ad18-120">PARAMETERS</span></span>

### <span data-ttu-id="5ad18-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5ad18-121">-ApiId</span></span>
<span data-ttu-id="5ad18-122">Especifica o identificador de uma API existente.</span><span class="sxs-lookup"><span data-stu-id="5ad18-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="5ad18-123">Se você especificar esse parâmetro, o cmdlet removerá a política de escopo de API.</span><span class="sxs-lookup"><span data-stu-id="5ad18-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad18-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="5ad18-124">-Context</span></span>
<span data-ttu-id="5ad18-125">Especifica a instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5ad18-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5ad18-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5ad18-126">-OperationId</span></span>
<span data-ttu-id="5ad18-127">Especifica o identificador de uma operação existente.</span><span class="sxs-lookup"><span data-stu-id="5ad18-127">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="5ad18-128">Se você especificar esse parâmetro com o parâmetro *ApiId* , esse cmdlet removerá a política de escopo de operação.</span><span class="sxs-lookup"><span data-stu-id="5ad18-128">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad18-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ad18-129">-PassThru</span></span>
<span data-ttu-id="5ad18-130">Indica que esse cmdlet retorna um valor de $True, se tiver êxito, ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="5ad18-130">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="5ad18-131">-ProductId</span><span class="sxs-lookup"><span data-stu-id="5ad18-131">-ProductId</span></span>
<span data-ttu-id="5ad18-132">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="5ad18-132">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="5ad18-133">Se você especificar esse parâmetro, o cmdlet removerá a política de escopo do produto.</span><span class="sxs-lookup"><span data-stu-id="5ad18-133">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad18-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5ad18-134">-Confirm</span></span>
<span data-ttu-id="5ad18-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ad18-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ad18-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ad18-136">-WhatIf</span></span>
<span data-ttu-id="5ad18-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5ad18-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ad18-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ad18-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ad18-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ad18-139">-DefaultProfile</span></span>
<span data-ttu-id="5ad18-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ad18-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ad18-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ad18-141">CommonParameters</span></span>
<span data-ttu-id="5ad18-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ad18-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ad18-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ad18-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ad18-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ad18-144">INPUTS</span></span>

## <span data-ttu-id="5ad18-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ad18-145">OUTPUTS</span></span>

### <span data-ttu-id="5ad18-146">Booliana</span><span class="sxs-lookup"><span data-stu-id="5ad18-146">Boolean</span></span>

## <span data-ttu-id="5ad18-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ad18-147">NOTES</span></span>

## <span data-ttu-id="5ad18-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ad18-148">RELATED LINKS</span></span>

[<span data-ttu-id="5ad18-149">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5ad18-149">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="5ad18-150">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5ad18-150">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


