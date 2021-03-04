---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 43a8d9969668abd96783fd766d4f99edb4b89e19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890894"
---
# <span data-ttu-id="05028-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="05028-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="05028-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05028-102">SYNOPSIS</span></span>
<span data-ttu-id="05028-103">Cria um novo Valor Nomeado.</span><span class="sxs-lookup"><span data-stu-id="05028-103">Creates new Named Value.</span></span>

## <span data-ttu-id="05028-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="05028-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05028-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="05028-105">DESCRIPTION</span></span>
<span data-ttu-id="05028-106">O cmdlet **New-AzApiManagementNamedValue** cria um Gerenciamento de API do Azure **denominado Valor**.</span><span class="sxs-lookup"><span data-stu-id="05028-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="05028-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05028-107">EXAMPLES</span></span>

### <span data-ttu-id="05028-108">Exemplo 1: Criar um valor nomeado que inclui marcas</span><span class="sxs-lookup"><span data-stu-id="05028-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="05028-109">O primeiro comando atribui dois valores à $Tags variável.</span><span class="sxs-lookup"><span data-stu-id="05028-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="05028-110">O segundo comando cria um valor nomeado e atribui as cadeias de caracteres $Tags como marcas na propriedade.</span><span class="sxs-lookup"><span data-stu-id="05028-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="05028-111">Exemplo 2: Criar um valor nomeado que tenha um valor secreto</span><span class="sxs-lookup"><span data-stu-id="05028-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="05028-112">Este comando cria um **Valor Nomeado** que tem um valor criptografado.</span><span class="sxs-lookup"><span data-stu-id="05028-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="05028-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="05028-113">PARAMETERS</span></span>

### <span data-ttu-id="05028-114">-Context</span><span class="sxs-lookup"><span data-stu-id="05028-114">-Context</span></span>
<span data-ttu-id="05028-115">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="05028-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="05028-116">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="05028-116">This parameter is required.</span></span>

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

### <span data-ttu-id="05028-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05028-117">-DefaultProfile</span></span>
<span data-ttu-id="05028-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05028-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05028-119">-Name</span><span class="sxs-lookup"><span data-stu-id="05028-119">-Name</span></span>
<span data-ttu-id="05028-120">Nome do valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="05028-120">Name of the named value.</span></span>
<span data-ttu-id="05028-121">O comprimento máximo é de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="05028-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="05028-122">Ele pode conter apenas letras, dígitos, ponto, traço e caracteres de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="05028-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="05028-123">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="05028-123">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05028-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="05028-124">-NamedValueId</span></span>
<span data-ttu-id="05028-125">Identificador do novo valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="05028-125">Identifier of new named value.</span></span>
<span data-ttu-id="05028-126">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="05028-126">This parameter is optional.</span></span>
<span data-ttu-id="05028-127">Se não for especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="05028-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="05028-128">-Secret</span><span class="sxs-lookup"><span data-stu-id="05028-128">-Secret</span></span>
<span data-ttu-id="05028-129">Determina se o valor é um segredo e deve ser criptografado ou não.</span><span class="sxs-lookup"><span data-stu-id="05028-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="05028-130">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="05028-130">This parameter is optional.</span></span>
<span data-ttu-id="05028-131">Valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="05028-131">Default Value is false.</span></span>

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

### <span data-ttu-id="05028-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="05028-132">-Tag</span></span>
<span data-ttu-id="05028-133">Marcas a serem associadas ao valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="05028-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="05028-134">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="05028-134">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05028-135">-Value</span><span class="sxs-lookup"><span data-stu-id="05028-135">-Value</span></span>
<span data-ttu-id="05028-136">Valor do valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="05028-136">Value of the named value.</span></span>
<span data-ttu-id="05028-137">Pode conter expressões de política.</span><span class="sxs-lookup"><span data-stu-id="05028-137">Can contain policy expressions.</span></span>
<span data-ttu-id="05028-138">O comprimento máximo é de 1000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="05028-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="05028-139">Ele pode não estar vazio ou consistir apenas em espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="05028-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="05028-140">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="05028-140">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05028-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05028-141">-Confirm</span></span>
<span data-ttu-id="05028-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05028-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05028-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05028-143">-WhatIf</span></span>
<span data-ttu-id="05028-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="05028-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05028-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05028-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05028-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05028-146">CommonParameters</span></span>
<span data-ttu-id="05028-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05028-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05028-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05028-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05028-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05028-149">INPUTS</span></span>

### <span data-ttu-id="05028-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="05028-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="05028-151">System.String</span><span class="sxs-lookup"><span data-stu-id="05028-151">System.String</span></span>

### <span data-ttu-id="05028-152">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="05028-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="05028-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="05028-153">System.String[]</span></span>

## <span data-ttu-id="05028-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="05028-154">OUTPUTS</span></span>

### <span data-ttu-id="05028-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="05028-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="05028-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="05028-156">NOTES</span></span>

## <span data-ttu-id="05028-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05028-157">RELATED LINKS</span></span>
