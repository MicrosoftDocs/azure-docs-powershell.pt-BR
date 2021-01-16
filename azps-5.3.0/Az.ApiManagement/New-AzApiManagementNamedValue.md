---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272222"
---
# <span data-ttu-id="9249e-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="9249e-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="9249e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9249e-102">SYNOPSIS</span></span>
<span data-ttu-id="9249e-103">Cria um novo valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="9249e-103">Creates new Named Value.</span></span>

## <span data-ttu-id="9249e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9249e-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9249e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9249e-105">DESCRIPTION</span></span>
<span data-ttu-id="9249e-106">O cmdlet **New-AzApiManagementNamedValue** cria um **valor nomeado** de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="9249e-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="9249e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9249e-107">EXAMPLES</span></span>

### <span data-ttu-id="9249e-108">Exemplo 1: criar um valor nomeado que inclua marcas</span><span class="sxs-lookup"><span data-stu-id="9249e-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="9249e-109">O primeiro comando atribui dois valores à variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="9249e-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="9249e-110">O segundo comando cria um valor nomeado e atribui as cadeias de caracteres em $Tags como marcas na propriedade.</span><span class="sxs-lookup"><span data-stu-id="9249e-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="9249e-111">Exemplo 2: criar um valor nomeado com um valor secreto</span><span class="sxs-lookup"><span data-stu-id="9249e-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="9249e-112">Esse comando cria um **valor nomeado** que tem um valor que é criptografado.</span><span class="sxs-lookup"><span data-stu-id="9249e-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="9249e-113">OS</span><span class="sxs-lookup"><span data-stu-id="9249e-113">PARAMETERS</span></span>

### <span data-ttu-id="9249e-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9249e-114">-Context</span></span>
<span data-ttu-id="9249e-115">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9249e-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9249e-116">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="9249e-116">This parameter is required.</span></span>

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

### <span data-ttu-id="9249e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9249e-117">-DefaultProfile</span></span>
<span data-ttu-id="9249e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9249e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9249e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9249e-119">-Name</span></span>
<span data-ttu-id="9249e-120">Nome do valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="9249e-120">Name of the named value.</span></span>
<span data-ttu-id="9249e-121">O comprimento máximo é de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="9249e-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="9249e-122">Ele pode conter apenas letras, dígitos, ponto, traço e sublinhado de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9249e-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="9249e-123">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="9249e-123">This parameter is required.</span></span>

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

### <span data-ttu-id="9249e-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="9249e-124">-NamedValueId</span></span>
<span data-ttu-id="9249e-125">Identificador do novo valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="9249e-125">Identifier of new named value.</span></span>
<span data-ttu-id="9249e-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9249e-126">This parameter is optional.</span></span>
<span data-ttu-id="9249e-127">Se não for especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="9249e-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="9249e-128">-Segredo</span><span class="sxs-lookup"><span data-stu-id="9249e-128">-Secret</span></span>
<span data-ttu-id="9249e-129">Determina se o valor é um segredo e se deve ser criptografado ou não.</span><span class="sxs-lookup"><span data-stu-id="9249e-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="9249e-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9249e-130">This parameter is optional.</span></span>
<span data-ttu-id="9249e-131">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="9249e-131">Default Value is false.</span></span>

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

### <span data-ttu-id="9249e-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="9249e-132">-Tag</span></span>
<span data-ttu-id="9249e-133">Marcas a serem associadas ao valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="9249e-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="9249e-134">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9249e-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="9249e-135">-Valor</span><span class="sxs-lookup"><span data-stu-id="9249e-135">-Value</span></span>
<span data-ttu-id="9249e-136">Valor do valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="9249e-136">Value of the named value.</span></span>
<span data-ttu-id="9249e-137">Pode conter expressões de política.</span><span class="sxs-lookup"><span data-stu-id="9249e-137">Can contain policy expressions.</span></span>
<span data-ttu-id="9249e-138">O comprimento máximo é de 1000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="9249e-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="9249e-139">Ele pode não estar vazio ou consistir somente em espaços em branco.</span><span class="sxs-lookup"><span data-stu-id="9249e-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="9249e-140">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="9249e-140">This parameter is required.</span></span>

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

### <span data-ttu-id="9249e-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9249e-141">-Confirm</span></span>
<span data-ttu-id="9249e-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9249e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9249e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9249e-143">-WhatIf</span></span>
<span data-ttu-id="9249e-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9249e-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9249e-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9249e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9249e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9249e-146">CommonParameters</span></span>
<span data-ttu-id="9249e-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9249e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9249e-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9249e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9249e-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9249e-149">INPUTS</span></span>

### <span data-ttu-id="9249e-150">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9249e-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9249e-151">System. String</span><span class="sxs-lookup"><span data-stu-id="9249e-151">System.String</span></span>

### <span data-ttu-id="9249e-152">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9249e-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9249e-153">System. String []</span><span class="sxs-lookup"><span data-stu-id="9249e-153">System.String[]</span></span>

## <span data-ttu-id="9249e-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9249e-154">OUTPUTS</span></span>

### <span data-ttu-id="9249e-155">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="9249e-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="9249e-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9249e-156">NOTES</span></span>

## <span data-ttu-id="9249e-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9249e-157">RELATED LINKS</span></span>
