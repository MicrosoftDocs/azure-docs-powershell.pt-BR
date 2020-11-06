---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: fcf88fcb9b54adec01b8a04b50f557b6a74e7ca8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426517"
---
# <span data-ttu-id="46081-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="46081-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="46081-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46081-102">SYNOPSIS</span></span>
<span data-ttu-id="46081-103">Obtém a política de escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="46081-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46081-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46081-104">SYNTAX</span></span>

### <span data-ttu-id="46081-105">GetTenantLevel (padrão)</span><span class="sxs-lookup"><span data-stu-id="46081-105">GetTenantLevel (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46081-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="46081-106">GetProductLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46081-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="46081-107">GetApiLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46081-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="46081-108">GetOperationLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46081-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46081-109">DESCRIPTION</span></span>
<span data-ttu-id="46081-110">O cmdlet **Get-AzureRmApiManagementPolicy** Obtém a política de escopo especificada.</span><span class="sxs-lookup"><span data-stu-id="46081-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="46081-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46081-111">EXAMPLES</span></span>

### <span data-ttu-id="46081-112">Exemplo 1: obter a política de nível de locatário</span><span class="sxs-lookup"><span data-stu-id="46081-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="46081-113">Esse comando obtém a política de nível de locatário e salva-a em um arquivo denominado tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="46081-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="46081-114">Exemplo 2: obter a política de escopo do produto</span><span class="sxs-lookup"><span data-stu-id="46081-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="46081-115">Este comando obtém a política de escopo do produto</span><span class="sxs-lookup"><span data-stu-id="46081-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="46081-116">Exemplo 3: obter a política de escopo de API</span><span class="sxs-lookup"><span data-stu-id="46081-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="46081-117">Este comando obtém a política de escopo de API.</span><span class="sxs-lookup"><span data-stu-id="46081-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="46081-118">Exemplo 4: obter a política de escopo de operação</span><span class="sxs-lookup"><span data-stu-id="46081-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="46081-119">Esse comando obtém a política de escopo da operação.</span><span class="sxs-lookup"><span data-stu-id="46081-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="46081-120">OS</span><span class="sxs-lookup"><span data-stu-id="46081-120">PARAMETERS</span></span>

### <span data-ttu-id="46081-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="46081-121">-ApiId</span></span>
<span data-ttu-id="46081-122">Especifica o identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="46081-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="46081-123">Se você especificar esse parâmetro, o cmdlet retornará a política de escopo de API.</span><span class="sxs-lookup"><span data-stu-id="46081-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46081-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="46081-124">-ApiRevision</span></span>
<span data-ttu-id="46081-125">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="46081-125">Identifier of API Revision.</span></span> <span data-ttu-id="46081-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="46081-126">This parameter is optional.</span></span> <span data-ttu-id="46081-127">Se não for especificado, a política será recuperada da revisão de API ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="46081-127">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46081-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="46081-128">-Context</span></span>
<span data-ttu-id="46081-129">Especifica uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="46081-129">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="46081-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46081-130">-DefaultProfile</span></span>
<span data-ttu-id="46081-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46081-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46081-132">-Force</span><span class="sxs-lookup"><span data-stu-id="46081-132">-Force</span></span>
<span data-ttu-id="46081-133">ps_force</span><span class="sxs-lookup"><span data-stu-id="46081-133">ps_force</span></span>

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

### <span data-ttu-id="46081-134">-Format</span><span class="sxs-lookup"><span data-stu-id="46081-134">-Format</span></span>
<span data-ttu-id="46081-135">Especifica o formato da política de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="46081-135">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="46081-136">O valor padrão para esse parâmetro é "application/vnd. ms-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="46081-136">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="46081-137">-OperationId</span><span class="sxs-lookup"><span data-stu-id="46081-137">-OperationId</span></span>
<span data-ttu-id="46081-138">Especifica o identificador da operação de API existente.</span><span class="sxs-lookup"><span data-stu-id="46081-138">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="46081-139">Se você especificar esse parâmetro com *ApiId* , o cmdlet retornará a política de escopo de operação.</span><span class="sxs-lookup"><span data-stu-id="46081-139">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46081-140">-ProductId</span><span class="sxs-lookup"><span data-stu-id="46081-140">-ProductId</span></span>
<span data-ttu-id="46081-141">Especifica o identificador de um produto existente.</span><span class="sxs-lookup"><span data-stu-id="46081-141">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="46081-142">Se você especificar esse parâmetro, o cmdlet retornará a política de escopo do produto.</span><span class="sxs-lookup"><span data-stu-id="46081-142">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46081-143">-Salvar como</span><span class="sxs-lookup"><span data-stu-id="46081-143">-SaveAs</span></span>
<span data-ttu-id="46081-144">Especifica o caminho do arquivo no qual o resultado será salvo.</span><span class="sxs-lookup"><span data-stu-id="46081-144">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="46081-145">Se você não especificar esse parâmetro, o resultado será canalizado como um Stinger.</span><span class="sxs-lookup"><span data-stu-id="46081-145">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="46081-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="46081-146">-Confirm</span></span>
<span data-ttu-id="46081-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46081-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46081-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46081-148">-WhatIf</span></span>
<span data-ttu-id="46081-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="46081-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46081-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46081-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46081-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46081-151">CommonParameters</span></span>
<span data-ttu-id="46081-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46081-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46081-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46081-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46081-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46081-154">INPUTS</span></span>

### <span data-ttu-id="46081-155">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="46081-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="46081-156">System. String</span><span class="sxs-lookup"><span data-stu-id="46081-156">System.String</span></span>

### <span data-ttu-id="46081-157">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="46081-157">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="46081-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46081-158">OUTPUTS</span></span>

### <span data-ttu-id="46081-159">System. String</span><span class="sxs-lookup"><span data-stu-id="46081-159">System.String</span></span>

## <span data-ttu-id="46081-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46081-160">NOTES</span></span>

## <span data-ttu-id="46081-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46081-161">RELATED LINKS</span></span>

[<span data-ttu-id="46081-162">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="46081-162">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="46081-163">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="46081-163">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


