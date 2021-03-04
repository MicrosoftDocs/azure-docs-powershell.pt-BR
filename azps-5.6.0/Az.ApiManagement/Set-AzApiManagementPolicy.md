---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: 3858d24bb0c714da0e48ad5834870ec5127eb5e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887054"
---
# <span data-ttu-id="bbccd-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bbccd-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="bbccd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbccd-102">SYNOPSIS</span></span>
<span data-ttu-id="bbccd-103">Define a política de escopo especificada para Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="bbccd-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="bbccd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bbccd-104">SYNTAX</span></span>

### <span data-ttu-id="bbccd-105">SetTenantLevel (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bbccd-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bbccd-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="bbccd-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbccd-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="bbccd-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbccd-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="bbccd-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbccd-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bbccd-109">DESCRIPTION</span></span>
<span data-ttu-id="bbccd-110">O cmdlet **Set-AzApiManagementPolicy** define a política de escopo especificada para Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="bbccd-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="bbccd-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bbccd-111">EXAMPLES</span></span>

### <span data-ttu-id="bbccd-112">Exemplo 1: definir a política de nível de locatário</span><span class="sxs-lookup"><span data-stu-id="bbccd-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="bbccd-113">Este comando define a política de nível de locatário de um arquivo chamado tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="bbccd-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="bbccd-114">Exemplo 2: definir uma política de escopo de produto</span><span class="sxs-lookup"><span data-stu-id="bbccd-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="bbccd-115">Este comando define a política de escopo do produto para Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="bbccd-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="bbccd-116">Exemplo 3: Definir política de escopo de API</span><span class="sxs-lookup"><span data-stu-id="bbccd-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="bbccd-117">Este comando define a política de escopo da API para Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="bbccd-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="bbccd-118">Exemplo 4: Definir política de escopo de operação</span><span class="sxs-lookup"><span data-stu-id="bbccd-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="bbccd-119">Este comando define a política de escopo de operação para o Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="bbccd-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="bbccd-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bbccd-120">PARAMETERS</span></span>

### <span data-ttu-id="bbccd-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bbccd-121">-ApiId</span></span>
<span data-ttu-id="bbccd-122">Especifica o identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="bbccd-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="bbccd-123">Se você especificar esse parâmetro, o cmdlet definirá a política de escopo da API.</span><span class="sxs-lookup"><span data-stu-id="bbccd-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="bbccd-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="bbccd-124">-ApiRevision</span></span>
<span data-ttu-id="bbccd-125">Identificador da Revisão da API.</span><span class="sxs-lookup"><span data-stu-id="bbccd-125">Identifier of API Revision.</span></span> <span data-ttu-id="bbccd-126">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="bbccd-126">This parameter is optional.</span></span> <span data-ttu-id="bbccd-127">Se não for especificada, a política será atualizada na revisão da api ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="bbccd-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="bbccd-128">-Context</span><span class="sxs-lookup"><span data-stu-id="bbccd-128">-Context</span></span>
<span data-ttu-id="bbccd-129">Especifica a instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="bbccd-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="bbccd-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbccd-130">-DefaultProfile</span></span>
<span data-ttu-id="bbccd-131">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bbccd-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbccd-132">-Format</span><span class="sxs-lookup"><span data-stu-id="bbccd-132">-Format</span></span>
<span data-ttu-id="bbccd-133">Especifica o formato da política.</span><span class="sxs-lookup"><span data-stu-id="bbccd-133">Specifies the format of the policy.</span></span> <span data-ttu-id="bbccd-134">Ao usar `application/vnd.ms-azure-apim.policy+xml` , as expressões contidas na política devem ser de escape XML.</span><span class="sxs-lookup"><span data-stu-id="bbccd-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="bbccd-135">Ao `application/vnd.ms-azure-apim.policy.raw+xml` usá-la, **não** é necessário que a política escape de XML.</span><span class="sxs-lookup"><span data-stu-id="bbccd-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="bbccd-136">O valor padrão é `application/vnd.ms-azure-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="bbccd-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="bbccd-137">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="bbccd-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="bbccd-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="bbccd-138">-OperationId</span></span>
<span data-ttu-id="bbccd-139">Especifica o identificador da operação existente.</span><span class="sxs-lookup"><span data-stu-id="bbccd-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="bbccd-140">Se especificado com ApiId, definirá a política de escopo de operação.</span><span class="sxs-lookup"><span data-stu-id="bbccd-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="bbccd-141">Esses parâmetros são necessários.</span><span class="sxs-lookup"><span data-stu-id="bbccd-141">This parameters is required.</span></span>

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

### <span data-ttu-id="bbccd-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbccd-142">-PassThru</span></span>
<span data-ttu-id="bbccd-143">passthru</span><span class="sxs-lookup"><span data-stu-id="bbccd-143">passthru</span></span>

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

### <span data-ttu-id="bbccd-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="bbccd-144">-Policy</span></span>
<span data-ttu-id="bbccd-145">Especifica o documento de política como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bbccd-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="bbccd-146">Esse parâmetro será necessário se *PolicyFilePath* não for especificado.</span><span class="sxs-lookup"><span data-stu-id="bbccd-146">This parameter is required if the -*PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="bbccd-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="bbccd-147">-PolicyFilePath</span></span>
<span data-ttu-id="bbccd-148">Especifica o caminho do arquivo de documento de política.</span><span class="sxs-lookup"><span data-stu-id="bbccd-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="bbccd-149">Esse parâmetro é necessário se o *parâmetro Policy* não for especificado.</span><span class="sxs-lookup"><span data-stu-id="bbccd-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="bbccd-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="bbccd-150">-PolicyUrl</span></span>
<span data-ttu-id="bbccd-151">A URL onde o documento de Política está hospedado.</span><span class="sxs-lookup"><span data-stu-id="bbccd-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="bbccd-152">Esse parâmetro será necessário se -Policy ou -PolicyFilePath não for especificado.</span><span class="sxs-lookup"><span data-stu-id="bbccd-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="bbccd-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="bbccd-153">-ProductId</span></span>
<span data-ttu-id="bbccd-154">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="bbccd-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="bbccd-155">Se esse parâmetro for especificado, o cmdlet define a política de escopo do produto.</span><span class="sxs-lookup"><span data-stu-id="bbccd-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="bbccd-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbccd-156">CommonParameters</span></span>
<span data-ttu-id="bbccd-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbccd-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbccd-158">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbccd-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbccd-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbccd-159">INPUTS</span></span>

### <span data-ttu-id="bbccd-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bbccd-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bbccd-161">System.String</span><span class="sxs-lookup"><span data-stu-id="bbccd-161">System.String</span></span>

### <span data-ttu-id="bbccd-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bbccd-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bbccd-163">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bbccd-163">OUTPUTS</span></span>

### <span data-ttu-id="bbccd-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bbccd-164">System.Boolean</span></span>

## <span data-ttu-id="bbccd-165">NOTES</span><span class="sxs-lookup"><span data-stu-id="bbccd-165">NOTES</span></span>

## <span data-ttu-id="bbccd-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbccd-166">RELATED LINKS</span></span>

[<span data-ttu-id="bbccd-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bbccd-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="bbccd-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bbccd-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)


