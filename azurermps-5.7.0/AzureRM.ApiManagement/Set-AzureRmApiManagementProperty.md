---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 89612136023173d2f725c8c4b286a270400f8c6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610135"
---
# <span data-ttu-id="e191d-101">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="e191d-101">Set-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="e191d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e191d-102">SYNOPSIS</span></span>
<span data-ttu-id="e191d-103">Modifica uma propriedade de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="e191d-103">Modifies an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e191d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e191d-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e191d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e191d-105">DESCRIPTION</span></span>
<span data-ttu-id="e191d-106">O cmdlet **set-AzureRmApiManagementProperty** modifica uma propriedade de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="e191d-106">The **Set-AzureRmApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="e191d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e191d-107">EXAMPLES</span></span>

### <span data-ttu-id="e191d-108">Exemplo 1: alterar as marcas em uma propriedade</span><span class="sxs-lookup"><span data-stu-id="e191d-108">Example 1: Change the tags on a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="e191d-109">O primeiro comando atribui dois valores à variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="e191d-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="e191d-110">O segundo comando modifica a propriedade que tem a ID Property11.</span><span class="sxs-lookup"><span data-stu-id="e191d-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="e191d-111">O comando atribui as cadeias de caracteres em $Tags como marcas na propriedade.</span><span class="sxs-lookup"><span data-stu-id="e191d-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="e191d-112">Exemplo 2: modificar uma propriedade para ter um valor secreto</span><span class="sxs-lookup"><span data-stu-id="e191d-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="e191d-113">Esse comando altera a propriedade a ser criptografada.</span><span class="sxs-lookup"><span data-stu-id="e191d-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="e191d-114">OS</span><span class="sxs-lookup"><span data-stu-id="e191d-114">PARAMETERS</span></span>

### <span data-ttu-id="e191d-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e191d-115">-Context</span></span>
<span data-ttu-id="e191d-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e191d-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e191d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e191d-117">-DefaultProfile</span></span>
<span data-ttu-id="e191d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e191d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e191d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e191d-119">-Name</span></span>
<span data-ttu-id="e191d-120">Especifica o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="e191d-120">Specifies the name of the property.</span></span>
<span data-ttu-id="e191d-121">O comprimento máximo é de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e191d-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="e191d-122">Os nomes contêm apenas letras, dígitos, ponto, traço e sublinhado caracteres.</span><span class="sxs-lookup"><span data-stu-id="e191d-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="e191d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e191d-123">-PassThru</span></span>
<span data-ttu-id="e191d-124">Indica que esse cmdlet retorna o **PsApiManagementProperty** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="e191d-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e191d-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="e191d-125">-PropertyId</span></span>
<span data-ttu-id="e191d-126">Especifica uma ID da propriedade que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="e191d-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e191d-127">-Segredo</span><span class="sxs-lookup"><span data-stu-id="e191d-127">-Secret</span></span>
<span data-ttu-id="e191d-128">Indica que o valor da propriedade é um segredo e deve ser criptografado.</span><span class="sxs-lookup"><span data-stu-id="e191d-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e191d-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="e191d-129">-Tag</span></span>
<span data-ttu-id="e191d-130">Marcas associadas a uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="e191d-130">Tags associated with a property.</span></span> <span data-ttu-id="e191d-131">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e191d-131">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e191d-132">-Valor</span><span class="sxs-lookup"><span data-stu-id="e191d-132">-Value</span></span>
<span data-ttu-id="e191d-133">Especifica um valor para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="e191d-133">Specifies a value for the property.</span></span>
<span data-ttu-id="e191d-134">Esse valor pode conter expressões de política.</span><span class="sxs-lookup"><span data-stu-id="e191d-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="e191d-135">O comprimento máximo é de 1000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e191d-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="e191d-136">O valor não pode estar vazio ou consistir apenas em um espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="e191d-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="e191d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e191d-137">CommonParameters</span></span>
<span data-ttu-id="e191d-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e191d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e191d-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e191d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e191d-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e191d-140">INPUTS</span></span>

### <span data-ttu-id="e191d-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e191d-141">None</span></span>
<span data-ttu-id="e191d-142">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e191d-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e191d-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e191d-143">OUTPUTS</span></span>

### <span data-ttu-id="e191d-144">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="e191d-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="e191d-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e191d-145">NOTES</span></span>

## <span data-ttu-id="e191d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e191d-146">RELATED LINKS</span></span>

[<span data-ttu-id="e191d-147">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="e191d-147">Get-AzureRmApiManagementProperty</span></span>](./Get-AzureRmApiManagementProperty.md)

[<span data-ttu-id="e191d-148">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="e191d-148">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="e191d-149">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="e191d-149">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)


