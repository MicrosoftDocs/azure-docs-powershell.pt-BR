---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: 49b86055c185dd474499cf8674a34668f69ee060
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597923"
---
# <span data-ttu-id="7bf47-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7bf47-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="7bf47-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bf47-102">SYNOPSIS</span></span>
<span data-ttu-id="7bf47-103">Modifica uma propriedade de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="7bf47-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="7bf47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bf47-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bf47-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7bf47-105">DESCRIPTION</span></span>
<span data-ttu-id="7bf47-106">O cmdlet **set-AzApiManagementProperty** modifica uma propriedade de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="7bf47-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="7bf47-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bf47-107">EXAMPLES</span></span>

### <span data-ttu-id="7bf47-108">Exemplo 1: alterar as marcas em uma propriedade</span><span class="sxs-lookup"><span data-stu-id="7bf47-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="7bf47-109">O primeiro comando atribui dois valores à variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="7bf47-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="7bf47-110">O segundo comando modifica a propriedade que tem a ID Property11.</span><span class="sxs-lookup"><span data-stu-id="7bf47-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="7bf47-111">O comando atribui as cadeias de caracteres em $Tags como marcas na propriedade.</span><span class="sxs-lookup"><span data-stu-id="7bf47-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="7bf47-112">Exemplo 2: modificar uma propriedade para ter um valor secreto</span><span class="sxs-lookup"><span data-stu-id="7bf47-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="7bf47-113">Esse comando altera a propriedade a ser criptografada.</span><span class="sxs-lookup"><span data-stu-id="7bf47-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="7bf47-114">OS</span><span class="sxs-lookup"><span data-stu-id="7bf47-114">PARAMETERS</span></span>

### <span data-ttu-id="7bf47-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7bf47-115">-Context</span></span>
<span data-ttu-id="7bf47-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7bf47-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7bf47-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bf47-117">-DefaultProfile</span></span>
<span data-ttu-id="7bf47-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7bf47-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bf47-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7bf47-119">-Name</span></span>
<span data-ttu-id="7bf47-120">Especifica o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="7bf47-120">Specifies the name of the property.</span></span>
<span data-ttu-id="7bf47-121">O comprimento máximo é de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7bf47-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="7bf47-122">Os nomes contêm apenas letras, dígitos, ponto, traço e sublinhado caracteres.</span><span class="sxs-lookup"><span data-stu-id="7bf47-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="7bf47-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bf47-123">-PassThru</span></span>
<span data-ttu-id="7bf47-124">Indica que esse cmdlet retorna o **PsApiManagementProperty** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="7bf47-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7bf47-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="7bf47-125">-PropertyId</span></span>
<span data-ttu-id="7bf47-126">Especifica uma ID da propriedade que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="7bf47-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7bf47-127">-Segredo</span><span class="sxs-lookup"><span data-stu-id="7bf47-127">-Secret</span></span>
<span data-ttu-id="7bf47-128">Indica que o valor da propriedade é um segredo e deve ser criptografado.</span><span class="sxs-lookup"><span data-stu-id="7bf47-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bf47-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="7bf47-129">-Tag</span></span>
<span data-ttu-id="7bf47-130">Marcas associadas a uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="7bf47-130">Tags associated with a property.</span></span> <span data-ttu-id="7bf47-131">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7bf47-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="7bf47-132">-Valor</span><span class="sxs-lookup"><span data-stu-id="7bf47-132">-Value</span></span>
<span data-ttu-id="7bf47-133">Especifica um valor para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="7bf47-133">Specifies a value for the property.</span></span>
<span data-ttu-id="7bf47-134">Esse valor pode conter expressões de política.</span><span class="sxs-lookup"><span data-stu-id="7bf47-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="7bf47-135">O comprimento máximo é de 1000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7bf47-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="7bf47-136">O valor não pode estar vazio ou consistir apenas em um espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="7bf47-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="7bf47-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7bf47-137">-Confirm</span></span>
<span data-ttu-id="7bf47-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bf47-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bf47-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bf47-139">-WhatIf</span></span>
<span data-ttu-id="7bf47-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7bf47-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bf47-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7bf47-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bf47-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bf47-142">CommonParameters</span></span>
<span data-ttu-id="7bf47-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bf47-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bf47-144">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bf47-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bf47-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7bf47-145">INPUTS</span></span>

### <span data-ttu-id="7bf47-146">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7bf47-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7bf47-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7bf47-147">System.String</span></span>

### <span data-ttu-id="7bf47-148">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7bf47-148">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7bf47-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="7bf47-149">System.String[]</span></span>

### <span data-ttu-id="7bf47-150">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7bf47-150">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7bf47-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7bf47-151">OUTPUTS</span></span>

### <span data-ttu-id="7bf47-152">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7bf47-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="7bf47-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7bf47-153">NOTES</span></span>

## <span data-ttu-id="7bf47-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bf47-154">RELATED LINKS</span></span>

[<span data-ttu-id="7bf47-155">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7bf47-155">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="7bf47-156">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7bf47-156">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="7bf47-157">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7bf47-157">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


