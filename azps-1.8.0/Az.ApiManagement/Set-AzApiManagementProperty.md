---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: b12a904be944b4a6338ad0bf34a4c906382cb910
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771326"
---
# <span data-ttu-id="0bd2a-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="0bd2a-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="0bd2a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0bd2a-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd2a-103">Modifica uma propriedade de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="0bd2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bd2a-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0bd2a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0bd2a-105">DESCRIPTION</span></span>
<span data-ttu-id="0bd2a-106">O cmdlet **set-AzApiManagementProperty** modifica uma propriedade de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="0bd2a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0bd2a-107">EXAMPLES</span></span>

### <span data-ttu-id="0bd2a-108">Exemplo 1: alterar as marcas em uma propriedade</span><span class="sxs-lookup"><span data-stu-id="0bd2a-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="0bd2a-109">O primeiro comando atribui dois valores à variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="0bd2a-110">O segundo comando modifica a propriedade que tem a ID Property11.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="0bd2a-111">O comando atribui as cadeias de caracteres em $Tags como marcas na propriedade.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="0bd2a-112">Exemplo 2: modificar uma propriedade para ter um valor secreto</span><span class="sxs-lookup"><span data-stu-id="0bd2a-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="0bd2a-113">Esse comando altera a propriedade a ser criptografada.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="0bd2a-114">OS</span><span class="sxs-lookup"><span data-stu-id="0bd2a-114">PARAMETERS</span></span>

### <span data-ttu-id="0bd2a-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="0bd2a-115">-Context</span></span>
<span data-ttu-id="0bd2a-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0bd2a-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0bd2a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bd2a-117">-DefaultProfile</span></span>
<span data-ttu-id="0bd2a-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bd2a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0bd2a-119">-Name</span></span>
<span data-ttu-id="0bd2a-120">Especifica o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-120">Specifies the name of the property.</span></span>
<span data-ttu-id="0bd2a-121">O comprimento máximo é de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="0bd2a-122">Os nomes contêm apenas letras, dígitos, ponto, traço e sublinhado caracteres.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="0bd2a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bd2a-123">-PassThru</span></span>
<span data-ttu-id="0bd2a-124">Indica que esse cmdlet retorna o **PsApiManagementProperty** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0bd2a-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="0bd2a-125">-PropertyId</span></span>
<span data-ttu-id="0bd2a-126">Especifica uma ID da propriedade que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0bd2a-127">-Segredo</span><span class="sxs-lookup"><span data-stu-id="0bd2a-127">-Secret</span></span>
<span data-ttu-id="0bd2a-128">Indica que o valor da propriedade é um segredo e deve ser criptografado.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-128">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="0bd2a-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="0bd2a-129">-Tag</span></span>
<span data-ttu-id="0bd2a-130">Marcas associadas a uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-130">Tags associated with a property.</span></span> <span data-ttu-id="0bd2a-131">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="0bd2a-132">-Valor</span><span class="sxs-lookup"><span data-stu-id="0bd2a-132">-Value</span></span>
<span data-ttu-id="0bd2a-133">Especifica um valor para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-133">Specifies a value for the property.</span></span>
<span data-ttu-id="0bd2a-134">Esse valor pode conter expressões de política.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="0bd2a-135">O comprimento máximo é de 1000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="0bd2a-136">O valor não pode estar vazio ou consistir apenas em um espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="0bd2a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd2a-137">CommonParameters</span></span>
<span data-ttu-id="0bd2a-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd2a-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bd2a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd2a-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0bd2a-140">INPUTS</span></span>

### <span data-ttu-id="0bd2a-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0bd2a-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0bd2a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0bd2a-142">System.String</span></span>

### <span data-ttu-id="0bd2a-143">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0bd2a-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0bd2a-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="0bd2a-144">System.String[]</span></span>

### <span data-ttu-id="0bd2a-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0bd2a-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0bd2a-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0bd2a-146">OUTPUTS</span></span>

### <span data-ttu-id="0bd2a-147">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="0bd2a-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="0bd2a-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0bd2a-148">NOTES</span></span>

## <span data-ttu-id="0bd2a-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bd2a-149">RELATED LINKS</span></span>

[<span data-ttu-id="0bd2a-150">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="0bd2a-150">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="0bd2a-151">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="0bd2a-151">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="0bd2a-152">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="0bd2a-152">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


