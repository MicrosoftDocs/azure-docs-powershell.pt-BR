---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 16eed643397245fa54b2876430042335762ea048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431252"
---
# <span data-ttu-id="6243b-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6243b-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="6243b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6243b-102">SYNOPSIS</span></span>
<span data-ttu-id="6243b-103">Obtém a política de escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="6243b-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6243b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6243b-104">SYNTAX</span></span>

### <span data-ttu-id="6243b-105">Nível do locatário (padrão)</span><span class="sxs-lookup"><span data-stu-id="6243b-105">Tenant level (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6243b-106">Nível do produto</span><span class="sxs-lookup"><span data-stu-id="6243b-106">Product level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6243b-107">Nível de API</span><span class="sxs-lookup"><span data-stu-id="6243b-107">API level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6243b-108">Nível de operação</span><span class="sxs-lookup"><span data-stu-id="6243b-108">Operation level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6243b-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6243b-109">DESCRIPTION</span></span>
<span data-ttu-id="6243b-110">O cmdlet **Get-AzureRmApiManagementPolicy** Obtém a política de escopo especificada.</span><span class="sxs-lookup"><span data-stu-id="6243b-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="6243b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6243b-111">EXAMPLES</span></span>

### <span data-ttu-id="6243b-112">Exemplo 1: obter a política de nível de locatário</span><span class="sxs-lookup"><span data-stu-id="6243b-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="6243b-113">Esse comando obtém a política de nível de locatário e salva-a em um arquivo denominado tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="6243b-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="6243b-114">Exemplo 2: obter a política de escopo do produto</span><span class="sxs-lookup"><span data-stu-id="6243b-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="6243b-115">Este comando obtém a política de escopo do produto</span><span class="sxs-lookup"><span data-stu-id="6243b-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="6243b-116">Exemplo 3: obter a política de escopo de API</span><span class="sxs-lookup"><span data-stu-id="6243b-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

<span data-ttu-id="6243b-117">Este comando obtém a política de escopo de API.</span><span class="sxs-lookup"><span data-stu-id="6243b-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="6243b-118">Exemplo 4: obter a política de escopo de operação</span><span class="sxs-lookup"><span data-stu-id="6243b-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="6243b-119">Esse comando obtém a política de escopo da operação.</span><span class="sxs-lookup"><span data-stu-id="6243b-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="6243b-120">OS</span><span class="sxs-lookup"><span data-stu-id="6243b-120">PARAMETERS</span></span>

### <span data-ttu-id="6243b-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6243b-121">-ApiId</span></span>
<span data-ttu-id="6243b-122">Especifica o identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="6243b-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="6243b-123">Se você especificar esse parâmetro, o cmdlet retornará a política de escopo de API.</span><span class="sxs-lookup"><span data-stu-id="6243b-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

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

### <span data-ttu-id="6243b-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="6243b-124">-Context</span></span>
<span data-ttu-id="6243b-125">Especifica uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="6243b-125">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="6243b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="6243b-126">-Force</span></span>
<span data-ttu-id="6243b-127">ps_force</span><span class="sxs-lookup"><span data-stu-id="6243b-127">ps_force</span></span>

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

### <span data-ttu-id="6243b-128">-Format</span><span class="sxs-lookup"><span data-stu-id="6243b-128">-Format</span></span>
<span data-ttu-id="6243b-129">Especifica o formato da política de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="6243b-129">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="6243b-130">O valor padrão para esse parâmetro é "application/vnd. ms-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="6243b-130">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6243b-131">-OperationId</span><span class="sxs-lookup"><span data-stu-id="6243b-131">-OperationId</span></span>
<span data-ttu-id="6243b-132">Especifica o identificador da operação de API existente.</span><span class="sxs-lookup"><span data-stu-id="6243b-132">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="6243b-133">Se você especificar esse parâmetro com *ApiId* , o cmdlet retornará a política de escopo de operação.</span><span class="sxs-lookup"><span data-stu-id="6243b-133">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

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

### <span data-ttu-id="6243b-134">-ProductId</span><span class="sxs-lookup"><span data-stu-id="6243b-134">-ProductId</span></span>
<span data-ttu-id="6243b-135">Especifica o identificador de um produto existente.</span><span class="sxs-lookup"><span data-stu-id="6243b-135">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="6243b-136">Se você especificar esse parâmetro, o cmdlet retornará a política de escopo do produto.</span><span class="sxs-lookup"><span data-stu-id="6243b-136">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

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

### <span data-ttu-id="6243b-137">-Salvar como</span><span class="sxs-lookup"><span data-stu-id="6243b-137">-SaveAs</span></span>
<span data-ttu-id="6243b-138">Especifica o caminho do arquivo no qual o resultado será salvo.</span><span class="sxs-lookup"><span data-stu-id="6243b-138">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="6243b-139">Se você não especificar esse parâmetro, o resultado será canalizado como um Stinger.</span><span class="sxs-lookup"><span data-stu-id="6243b-139">If you do not specify this parameter the result is pipelined as a sting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6243b-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6243b-140">-Confirm</span></span>
<span data-ttu-id="6243b-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6243b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6243b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6243b-142">-WhatIf</span></span>
<span data-ttu-id="6243b-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6243b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6243b-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6243b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6243b-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6243b-145">-DefaultProfile</span></span>
<span data-ttu-id="6243b-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6243b-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6243b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6243b-147">CommonParameters</span></span>
<span data-ttu-id="6243b-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6243b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6243b-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6243b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6243b-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6243b-150">INPUTS</span></span>

## <span data-ttu-id="6243b-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6243b-151">OUTPUTS</span></span>

### <span data-ttu-id="6243b-152">String</span><span class="sxs-lookup"><span data-stu-id="6243b-152">String</span></span>

## <span data-ttu-id="6243b-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6243b-153">NOTES</span></span>

## <span data-ttu-id="6243b-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6243b-154">RELATED LINKS</span></span>

[<span data-ttu-id="6243b-155">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6243b-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="6243b-156">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6243b-156">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


