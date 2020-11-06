---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 75bb963195244a5a1a27ca004eb2795b6b5bb556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427336"
---
# <span data-ttu-id="1ebf5-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1ebf5-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="1ebf5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ebf5-102">SYNOPSIS</span></span>
<span data-ttu-id="1ebf5-103">Define a política de escopo especificada para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ebf5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ebf5-104">SYNTAX</span></span>

### <span data-ttu-id="1ebf5-105">SetTenantLevel (padrão)</span><span class="sxs-lookup"><span data-stu-id="1ebf5-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ebf5-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="1ebf5-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ebf5-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="1ebf5-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ebf5-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="1ebf5-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ebf5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ebf5-109">DESCRIPTION</span></span>
<span data-ttu-id="1ebf5-110">O cmdlet **set-AzureRmApiManagementPolicy** define a política de escopo especificada para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="1ebf5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ebf5-111">EXAMPLES</span></span>

### <span data-ttu-id="1ebf5-112">Exemplo 1: definir a política de nível de locatário</span><span class="sxs-lookup"><span data-stu-id="1ebf5-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="1ebf5-113">Esse comando define a política de nível de locatário de um arquivo chamado tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="1ebf5-114">Exemplo 2: definir uma política de escopo de produto</span><span class="sxs-lookup"><span data-stu-id="1ebf5-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="1ebf5-115">Esse comando define a política de escopo de produto para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="1ebf5-116">Exemplo 3: definir política de escopo de API</span><span class="sxs-lookup"><span data-stu-id="1ebf5-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="1ebf5-117">Esse comando define a política de escopo de API para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="1ebf5-118">Exemplo 4: definir a política de escopo de operações</span><span class="sxs-lookup"><span data-stu-id="1ebf5-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="1ebf5-119">Este comando define a política de escopo de operação para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="1ebf5-120">OS</span><span class="sxs-lookup"><span data-stu-id="1ebf5-120">PARAMETERS</span></span>

### <span data-ttu-id="1ebf5-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1ebf5-121">-ApiId</span></span>
<span data-ttu-id="1ebf5-122">Especifica o identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="1ebf5-123">Se você especificar esse parâmetro, o cmdlet define a política de escopo de API.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="1ebf5-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="1ebf5-124">-ApiRevision</span></span>
<span data-ttu-id="1ebf5-125">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-125">Identifier of API Revision.</span></span> <span data-ttu-id="1ebf5-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-126">This parameter is optional.</span></span> <span data-ttu-id="1ebf5-127">Se não for especificado, a política será atualizada na revisão de API ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="1ebf5-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1ebf5-128">-Context</span></span>
<span data-ttu-id="1ebf5-129">Especifica a instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="1ebf5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ebf5-130">-DefaultProfile</span></span>
<span data-ttu-id="1ebf5-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ebf5-132">-Format</span><span class="sxs-lookup"><span data-stu-id="1ebf5-132">-Format</span></span>
<span data-ttu-id="1ebf5-133">Especifica o formato da política.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-133">Specifies the format of the policy.</span></span> <span data-ttu-id="1ebf5-134">Ao usar `application/vnd.ms-azure-apim.policy+xml` , as expressões contidas na política devem ser de escape XML.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="1ebf5-135">Ao usar `application/vnd.ms-azure-apim.policy.raw+xml` , **não** é necessário que a política seja de saída XML.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="1ebf5-136">O valor padrão é `application/vnd.ms-azure-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="1ebf5-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="1ebf5-137">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/vnd.ms-azure-apim.policy.raw+xml, application/vnd.ms-azure-apim.policy+xml

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ebf5-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="1ebf5-138">-OperationId</span></span>
<span data-ttu-id="1ebf5-139">Especifica o identificador da operação existente.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="1ebf5-140">Se especificado com ApiId, a política de escopo de operação será definida.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="1ebf5-141">Estes parâmetros são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-141">This parameters is required.</span></span>

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

### <span data-ttu-id="1ebf5-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ebf5-142">-PassThru</span></span>
<span data-ttu-id="1ebf5-143">PassThru</span><span class="sxs-lookup"><span data-stu-id="1ebf5-143">passthru</span></span>

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

### <span data-ttu-id="1ebf5-144">-Política</span><span class="sxs-lookup"><span data-stu-id="1ebf5-144">-Policy</span></span>
<span data-ttu-id="1ebf5-145">Especifica o documento de política como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="1ebf5-146">Esse parâmetro será necessário se a- *PolicyFilePath* não for especificada.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="1ebf5-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="1ebf5-147">-PolicyFilePath</span></span>
<span data-ttu-id="1ebf5-148">Especifica o caminho do arquivo do documento da política.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="1ebf5-149">Esse parâmetro será necessário se o parâmetro *política* não for especificado.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="1ebf5-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="1ebf5-150">-PolicyUrl</span></span>
<span data-ttu-id="1ebf5-151">A URL na qual o documento de política está hospedado.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="1ebf5-152">Esse parâmetro será obrigatório se-Policy ou-PolicyFilePath não for especificado.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="1ebf5-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1ebf5-153">-ProductId</span></span>
<span data-ttu-id="1ebf5-154">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="1ebf5-155">Se esse parâmetro for especificado, o cmdlet define a política de escopo do produto.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="1ebf5-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ebf5-156">CommonParameters</span></span>
<span data-ttu-id="1ebf5-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ebf5-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ebf5-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ebf5-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ebf5-159">INPUTS</span></span>

### <span data-ttu-id="1ebf5-160">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1ebf5-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1ebf5-161">System. String</span><span class="sxs-lookup"><span data-stu-id="1ebf5-161">System.String</span></span>

### <span data-ttu-id="1ebf5-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1ebf5-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1ebf5-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ebf5-163">OUTPUTS</span></span>

### <span data-ttu-id="1ebf5-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ebf5-164">System.Boolean</span></span>

## <span data-ttu-id="1ebf5-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ebf5-165">NOTES</span></span>

## <span data-ttu-id="1ebf5-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ebf5-166">RELATED LINKS</span></span>

[<span data-ttu-id="1ebf5-167">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1ebf5-167">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="1ebf5-168">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1ebf5-168">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


