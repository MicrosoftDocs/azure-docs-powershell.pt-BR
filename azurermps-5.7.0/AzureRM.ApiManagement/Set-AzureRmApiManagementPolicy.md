---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 0f9ee1c2190dbc3d657ecc52cd85b6af8b0cac4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602660"
---
# <span data-ttu-id="c7a14-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c7a14-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="c7a14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7a14-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a14-103">Define a política de escopo especificada para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c7a14-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7a14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7a14-104">SYNTAX</span></span>

### <span data-ttu-id="c7a14-105">SetTenantLevel (padrão)</span><span class="sxs-lookup"><span data-stu-id="c7a14-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7a14-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="c7a14-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7a14-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="c7a14-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7a14-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="c7a14-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7a14-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7a14-109">DESCRIPTION</span></span>
<span data-ttu-id="c7a14-110">O cmdlet **set-AzureRmApiManagementPolicy** define a política de escopo especificada para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c7a14-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="c7a14-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7a14-111">EXAMPLES</span></span>

### <span data-ttu-id="c7a14-112">Exemplo 1: definir a política de nível de locatário</span><span class="sxs-lookup"><span data-stu-id="c7a14-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="c7a14-113">Esse comando define a política de nível de locatário de um arquivo chamado tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="c7a14-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="c7a14-114">Exemplo 2: definir uma política de escopo de produto</span><span class="sxs-lookup"><span data-stu-id="c7a14-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="c7a14-115">Esse comando define a política de escopo de produto para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c7a14-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="c7a14-116">Exemplo 3: definir política de escopo de API</span><span class="sxs-lookup"><span data-stu-id="c7a14-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="c7a14-117">Esse comando define a política de escopo de API para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c7a14-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="c7a14-118">Exemplo 4: definir a política de escopo de operações</span><span class="sxs-lookup"><span data-stu-id="c7a14-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="c7a14-119">Este comando define a política de escopo de operação para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c7a14-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="c7a14-120">OS</span><span class="sxs-lookup"><span data-stu-id="c7a14-120">PARAMETERS</span></span>

### <span data-ttu-id="c7a14-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c7a14-121">-ApiId</span></span>
<span data-ttu-id="c7a14-122">Especifica o identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="c7a14-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="c7a14-123">Se você especificar esse parâmetro, o cmdlet define a política de escopo de API.</span><span class="sxs-lookup"><span data-stu-id="c7a14-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a14-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c7a14-124">-Context</span></span>
<span data-ttu-id="c7a14-125">Especifica a instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="c7a14-125">Specifies the instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a14-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a14-126">-DefaultProfile</span></span>
<span data-ttu-id="c7a14-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a14-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a14-128">-Format</span><span class="sxs-lookup"><span data-stu-id="c7a14-128">-Format</span></span>
<span data-ttu-id="c7a14-129">Especifica o formato da política.</span><span class="sxs-lookup"><span data-stu-id="c7a14-129">Specifies the format of the policy.</span></span>
<span data-ttu-id="c7a14-130">O valor padrão é "application/vnd. ms-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="c7a14-130">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a14-131">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c7a14-131">-OperationId</span></span>
<span data-ttu-id="c7a14-132">Especifica o identificador da operação existente.</span><span class="sxs-lookup"><span data-stu-id="c7a14-132">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="c7a14-133">Se especificado com ApiId, a política de escopo de operação será definida.</span><span class="sxs-lookup"><span data-stu-id="c7a14-133">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="c7a14-134">Estes parâmetros são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c7a14-134">This parameters is required.</span></span>

```yaml
Type: String
Parameter Sets: SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a14-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7a14-135">-PassThru</span></span>
<span data-ttu-id="c7a14-136">PassThru</span><span class="sxs-lookup"><span data-stu-id="c7a14-136">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a14-137">-Política</span><span class="sxs-lookup"><span data-stu-id="c7a14-137">-Policy</span></span>
<span data-ttu-id="c7a14-138">Especifica o documento de política como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c7a14-138">Specifies the policy document as a string.</span></span>
<span data-ttu-id="c7a14-139">Esse parâmetro será necessário se a- *PolicyFilePath* não for especificada.</span><span class="sxs-lookup"><span data-stu-id="c7a14-139">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a14-140">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="c7a14-140">-PolicyFilePath</span></span>
<span data-ttu-id="c7a14-141">Especifica o caminho do arquivo do documento da política.</span><span class="sxs-lookup"><span data-stu-id="c7a14-141">Specifies the policy document file path.</span></span>
<span data-ttu-id="c7a14-142">Esse parâmetro será necessário se o parâmetro *política* não for especificado.</span><span class="sxs-lookup"><span data-stu-id="c7a14-142">This parameter is required if the *Policy* parameter is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a14-143">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c7a14-143">-ProductId</span></span>
<span data-ttu-id="c7a14-144">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="c7a14-144">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="c7a14-145">Se esse parâmetro for especificado, o cmdlet define a política de escopo do produto.</span><span class="sxs-lookup"><span data-stu-id="c7a14-145">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a14-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a14-146">CommonParameters</span></span>
<span data-ttu-id="c7a14-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a14-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a14-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a14-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a14-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7a14-149">INPUTS</span></span>

### <span data-ttu-id="c7a14-150">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c7a14-150">None</span></span>
<span data-ttu-id="c7a14-151">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c7a14-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7a14-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7a14-152">OUTPUTS</span></span>

### <span data-ttu-id="c7a14-153">bool</span><span class="sxs-lookup"><span data-stu-id="c7a14-153">bool</span></span>

## <span data-ttu-id="c7a14-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7a14-154">NOTES</span></span>

## <span data-ttu-id="c7a14-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7a14-155">RELATED LINKS</span></span>

[<span data-ttu-id="c7a14-156">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c7a14-156">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="c7a14-157">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c7a14-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


