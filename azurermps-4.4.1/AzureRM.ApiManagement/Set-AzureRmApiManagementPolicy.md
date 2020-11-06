---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 8073df3946f5bf42ee8b0e5f2c7ae7881e905eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431209"
---
# <span data-ttu-id="69d6f-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="69d6f-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="69d6f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="69d6f-103">Define a política de escopo especificada para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="69d6f-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69d6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69d6f-104">SYNTAX</span></span>

### <span data-ttu-id="69d6f-105">Nível do locatário (padrão)</span><span class="sxs-lookup"><span data-stu-id="69d6f-105">Tenant level (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69d6f-106">Nível do produto</span><span class="sxs-lookup"><span data-stu-id="69d6f-106">Product level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69d6f-107">Nível de API</span><span class="sxs-lookup"><span data-stu-id="69d6f-107">API level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69d6f-108">Nível de operação</span><span class="sxs-lookup"><span data-stu-id="69d6f-108">Operation level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69d6f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69d6f-109">DESCRIPTION</span></span>
<span data-ttu-id="69d6f-110">O cmdlet **set-AzureRmApiManagementPolicy** define a política de escopo especificada para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="69d6f-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="69d6f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69d6f-111">EXAMPLES</span></span>

### <span data-ttu-id="69d6f-112">Exemplo 1: definir a política de nível de locatário</span><span class="sxs-lookup"><span data-stu-id="69d6f-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="69d6f-113">Esse comando define a política de nível de locatário de um arquivo chamado tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="69d6f-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="69d6f-114">Exemplo 2: definir uma política de escopo de produto</span><span class="sxs-lookup"><span data-stu-id="69d6f-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="69d6f-115">Esse comando define a política de escopo de produto para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="69d6f-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="69d6f-116">Exemplo 3: definir política de escopo de API</span><span class="sxs-lookup"><span data-stu-id="69d6f-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="69d6f-117">Esse comando define a política de escopo de API para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="69d6f-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="69d6f-118">Exemplo 4: definir a política de escopo de operações</span><span class="sxs-lookup"><span data-stu-id="69d6f-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="69d6f-119">Este comando define a política de escopo de operação para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="69d6f-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="69d6f-120">OS</span><span class="sxs-lookup"><span data-stu-id="69d6f-120">PARAMETERS</span></span>

### <span data-ttu-id="69d6f-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="69d6f-121">-ApiId</span></span>
<span data-ttu-id="69d6f-122">Especifica o identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="69d6f-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="69d6f-123">Se você especificar esse parâmetro, o cmdlet define a política de escopo de API.</span><span class="sxs-lookup"><span data-stu-id="69d6f-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="69d6f-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="69d6f-124">-Context</span></span>
<span data-ttu-id="69d6f-125">Especifica a instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="69d6f-125">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="69d6f-126">-Format</span><span class="sxs-lookup"><span data-stu-id="69d6f-126">-Format</span></span>
<span data-ttu-id="69d6f-127">Especifica o formato da política.</span><span class="sxs-lookup"><span data-stu-id="69d6f-127">Specifies the format of the policy.</span></span>
<span data-ttu-id="69d6f-128">O valor padrão é "application/vnd. ms-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="69d6f-128">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="69d6f-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="69d6f-129">-OperationId</span></span>
<span data-ttu-id="69d6f-130">Especifica o identificador da operação existente.</span><span class="sxs-lookup"><span data-stu-id="69d6f-130">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="69d6f-131">Se especificado com ApiId, a política de escopo de operação será definida.</span><span class="sxs-lookup"><span data-stu-id="69d6f-131">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="69d6f-132">Estes parâmetros são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="69d6f-132">This parameters is required.</span></span>

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

### <span data-ttu-id="69d6f-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69d6f-133">-PassThru</span></span>
<span data-ttu-id="69d6f-134">PassThru</span><span class="sxs-lookup"><span data-stu-id="69d6f-134">passthru</span></span>

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

### <span data-ttu-id="69d6f-135">-Política</span><span class="sxs-lookup"><span data-stu-id="69d6f-135">-Policy</span></span>
<span data-ttu-id="69d6f-136">Especifica o documento de política como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="69d6f-136">Specifies the policy document as a string.</span></span>
<span data-ttu-id="69d6f-137">Esse parâmetro será necessário se a- *PolicyFilePath* não for especificada.</span><span class="sxs-lookup"><span data-stu-id="69d6f-137">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="69d6f-138">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="69d6f-138">-PolicyFilePath</span></span>
<span data-ttu-id="69d6f-139">Especifica o caminho do arquivo do documento da política.</span><span class="sxs-lookup"><span data-stu-id="69d6f-139">Specifies the policy document file path.</span></span>
<span data-ttu-id="69d6f-140">Esse parâmetro será necessário se o parâmetro *política* não for especificado.</span><span class="sxs-lookup"><span data-stu-id="69d6f-140">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="69d6f-141">-ProductId</span><span class="sxs-lookup"><span data-stu-id="69d6f-141">-ProductId</span></span>
<span data-ttu-id="69d6f-142">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="69d6f-142">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="69d6f-143">Se esse parâmetro for especificado, o cmdlet define a política de escopo do produto.</span><span class="sxs-lookup"><span data-stu-id="69d6f-143">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="69d6f-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69d6f-144">-DefaultProfile</span></span>
<span data-ttu-id="69d6f-145">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69d6f-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69d6f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69d6f-146">CommonParameters</span></span>
<span data-ttu-id="69d6f-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69d6f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69d6f-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69d6f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69d6f-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69d6f-149">INPUTS</span></span>

## <span data-ttu-id="69d6f-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69d6f-150">OUTPUTS</span></span>

### <span data-ttu-id="69d6f-151">bool</span><span class="sxs-lookup"><span data-stu-id="69d6f-151">bool</span></span>

## <span data-ttu-id="69d6f-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69d6f-152">NOTES</span></span>

## <span data-ttu-id="69d6f-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69d6f-153">RELATED LINKS</span></span>

[<span data-ttu-id="69d6f-154">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="69d6f-154">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="69d6f-155">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="69d6f-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


