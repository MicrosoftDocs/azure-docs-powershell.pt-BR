---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: 7398687bed785b0152b991656baf2784df204ed6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597927"
---
# <span data-ttu-id="78453-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="78453-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="78453-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78453-102">SYNOPSIS</span></span>
<span data-ttu-id="78453-103">Define a política de escopo especificada para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="78453-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="78453-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78453-104">SYNTAX</span></span>

### <span data-ttu-id="78453-105">SetTenantLevel (padrão)</span><span class="sxs-lookup"><span data-stu-id="78453-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78453-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="78453-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78453-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="78453-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78453-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="78453-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78453-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78453-109">DESCRIPTION</span></span>
<span data-ttu-id="78453-110">O cmdlet **set-AzApiManagementPolicy** define a política de escopo especificada para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="78453-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="78453-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78453-111">EXAMPLES</span></span>

### <span data-ttu-id="78453-112">Exemplo 1: definir a política de nível de locatário</span><span class="sxs-lookup"><span data-stu-id="78453-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="78453-113">Esse comando define a política de nível de locatário de um arquivo chamado tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="78453-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="78453-114">Exemplo 2: definir uma política de escopo de produto</span><span class="sxs-lookup"><span data-stu-id="78453-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="78453-115">Esse comando define a política de escopo de produto para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="78453-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="78453-116">Exemplo 3: definir política de escopo de API</span><span class="sxs-lookup"><span data-stu-id="78453-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="78453-117">Esse comando define a política de escopo de API para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="78453-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="78453-118">Exemplo 4: definir a política de escopo de operações</span><span class="sxs-lookup"><span data-stu-id="78453-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="78453-119">Este comando define a política de escopo de operação para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="78453-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="78453-120">OS</span><span class="sxs-lookup"><span data-stu-id="78453-120">PARAMETERS</span></span>

### <span data-ttu-id="78453-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="78453-121">-ApiId</span></span>
<span data-ttu-id="78453-122">Especifica o identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="78453-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="78453-123">Se você especificar esse parâmetro, o cmdlet define a política de escopo de API.</span><span class="sxs-lookup"><span data-stu-id="78453-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78453-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="78453-124">-ApiRevision</span></span>
<span data-ttu-id="78453-125">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="78453-125">Identifier of API Revision.</span></span> <span data-ttu-id="78453-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="78453-126">This parameter is optional.</span></span> <span data-ttu-id="78453-127">Se não for especificado, a política será atualizada na revisão de API ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="78453-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78453-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="78453-128">-Context</span></span>
<span data-ttu-id="78453-129">Especifica a instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="78453-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="78453-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78453-130">-DefaultProfile</span></span>
<span data-ttu-id="78453-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78453-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78453-132">-Format</span><span class="sxs-lookup"><span data-stu-id="78453-132">-Format</span></span>
<span data-ttu-id="78453-133">Especifica o formato da política.</span><span class="sxs-lookup"><span data-stu-id="78453-133">Specifies the format of the policy.</span></span> <span data-ttu-id="78453-134">Ao usar `application/vnd.ms-azure-apim.policy+xml` , as expressões contidas na política devem ser de escape XML.</span><span class="sxs-lookup"><span data-stu-id="78453-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="78453-135">Ao usar `application/vnd.ms-azure-apim.policy.raw+xml` , **não** é necessário que a política seja de saída XML.</span><span class="sxs-lookup"><span data-stu-id="78453-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="78453-136">O valor padrão é `application/vnd.ms-azure-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="78453-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="78453-137">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="78453-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="78453-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="78453-138">-OperationId</span></span>
<span data-ttu-id="78453-139">Especifica o identificador da operação existente.</span><span class="sxs-lookup"><span data-stu-id="78453-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="78453-140">Se especificado com ApiId, a política de escopo de operação será definida.</span><span class="sxs-lookup"><span data-stu-id="78453-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="78453-141">Estes parâmetros são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="78453-141">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78453-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78453-142">-PassThru</span></span>
<span data-ttu-id="78453-143">PassThru</span><span class="sxs-lookup"><span data-stu-id="78453-143">passthru</span></span>

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

### <span data-ttu-id="78453-144">-Política</span><span class="sxs-lookup"><span data-stu-id="78453-144">-Policy</span></span>
<span data-ttu-id="78453-145">Especifica o documento de política como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="78453-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="78453-146">Esse parâmetro será necessário se a- *PolicyFilePath* não for especificada.</span><span class="sxs-lookup"><span data-stu-id="78453-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="78453-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="78453-147">-PolicyFilePath</span></span>
<span data-ttu-id="78453-148">Especifica o caminho do arquivo do documento da política.</span><span class="sxs-lookup"><span data-stu-id="78453-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="78453-149">Esse parâmetro será necessário se o parâmetro *política* não for especificado.</span><span class="sxs-lookup"><span data-stu-id="78453-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="78453-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="78453-150">-PolicyUrl</span></span>
<span data-ttu-id="78453-151">A URL na qual o documento de política está hospedado.</span><span class="sxs-lookup"><span data-stu-id="78453-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="78453-152">Esse parâmetro será obrigatório se-Policy ou-PolicyFilePath não for especificado.</span><span class="sxs-lookup"><span data-stu-id="78453-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="78453-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="78453-153">-ProductId</span></span>
<span data-ttu-id="78453-154">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="78453-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="78453-155">Se esse parâmetro for especificado, o cmdlet define a política de escopo do produto.</span><span class="sxs-lookup"><span data-stu-id="78453-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78453-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78453-156">CommonParameters</span></span>
<span data-ttu-id="78453-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78453-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78453-158">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78453-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78453-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78453-159">INPUTS</span></span>

### <span data-ttu-id="78453-160">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="78453-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="78453-161">System. String</span><span class="sxs-lookup"><span data-stu-id="78453-161">System.String</span></span>

### <span data-ttu-id="78453-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="78453-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="78453-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78453-163">OUTPUTS</span></span>

### <span data-ttu-id="78453-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78453-164">System.Boolean</span></span>

## <span data-ttu-id="78453-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78453-165">NOTES</span></span>

## <span data-ttu-id="78453-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78453-166">RELATED LINKS</span></span>

[<span data-ttu-id="78453-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="78453-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="78453-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="78453-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)


