---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: 55ef0d4ef714c1d434915def403f5560244a3697
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611073"
---
# <span data-ttu-id="7b997-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7b997-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="7b997-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b997-102">SYNOPSIS</span></span>
<span data-ttu-id="7b997-103">Cria uma nova propriedade.</span><span class="sxs-lookup"><span data-stu-id="7b997-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b997-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b997-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b997-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b997-105">DESCRIPTION</span></span>
<span data-ttu-id="7b997-106">O cmdlet **New-AzureRmApiManagementProperty** cria uma **Propriedade** de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b997-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="7b997-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b997-107">EXAMPLES</span></span>

### <span data-ttu-id="7b997-108">Exemplo 1: criar uma propriedade que inclua marcas</span><span class="sxs-lookup"><span data-stu-id="7b997-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="7b997-109">O primeiro comando atribui dois valores à variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="7b997-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="7b997-110">O segundo comando cria uma propriedade e atribui as cadeias de caracteres em $Tags como marcas na propriedade.</span><span class="sxs-lookup"><span data-stu-id="7b997-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="7b997-111">Exemplo 2: criar uma propriedade com um valor secreto</span><span class="sxs-lookup"><span data-stu-id="7b997-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="7b997-112">Esse comando cria uma **Propriedade** que tem um valor criptografado.</span><span class="sxs-lookup"><span data-stu-id="7b997-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="7b997-113">OS</span><span class="sxs-lookup"><span data-stu-id="7b997-113">PARAMETERS</span></span>

### <span data-ttu-id="7b997-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7b997-114">-Context</span></span>
<span data-ttu-id="7b997-115">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7b997-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7b997-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b997-116">-DefaultProfile</span></span>
<span data-ttu-id="7b997-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b997-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="7b997-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b997-118">-Name</span></span>
<span data-ttu-id="7b997-119">Especifica o nome da propriedade que esse cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="7b997-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="7b997-120">O comprimento máximo é de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7b997-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="7b997-121">Os nomes contêm apenas letras, dígitos, ponto, traço e sublinhado caracteres.</span><span class="sxs-lookup"><span data-stu-id="7b997-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="7b997-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="7b997-122">-PropertyId</span></span>
<span data-ttu-id="7b997-123">Especifica uma ID para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="7b997-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="7b997-124">O comprimento máximo é de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7b997-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="7b997-125">Se você não especificar uma ID, esse cmdlet gerará uma.</span><span class="sxs-lookup"><span data-stu-id="7b997-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="7b997-126">-Segredo</span><span class="sxs-lookup"><span data-stu-id="7b997-126">-Secret</span></span>
<span data-ttu-id="7b997-127">Indica que o valor da propriedade é um segredo e deve ser criptografado.</span><span class="sxs-lookup"><span data-stu-id="7b997-127">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="7b997-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="7b997-128">-Tag</span></span>
<span data-ttu-id="7b997-129">Marcas a serem associadas à propriedade.</span><span class="sxs-lookup"><span data-stu-id="7b997-129">Tags to be associated with Property.</span></span> <span data-ttu-id="7b997-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7b997-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="7b997-131">-Valor</span><span class="sxs-lookup"><span data-stu-id="7b997-131">-Value</span></span>
<span data-ttu-id="7b997-132">Especifica um valor para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="7b997-132">Specifies a value for the property.</span></span>
<span data-ttu-id="7b997-133">Esse valor pode conter expressões de política.</span><span class="sxs-lookup"><span data-stu-id="7b997-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="7b997-134">O comprimento máximo é de 1000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7b997-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="7b997-135">O valor não pode estar vazio ou consistir apenas em um espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="7b997-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="7b997-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b997-136">CommonParameters</span></span>
<span data-ttu-id="7b997-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b997-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b997-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b997-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b997-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b997-139">INPUTS</span></span>

### <span data-ttu-id="7b997-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7b997-140">None</span></span>
<span data-ttu-id="7b997-141">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="7b997-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b997-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b997-142">OUTPUTS</span></span>

### <span data-ttu-id="7b997-143">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7b997-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="7b997-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b997-144">NOTES</span></span>

## <span data-ttu-id="7b997-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b997-145">RELATED LINKS</span></span>

[<span data-ttu-id="7b997-146">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7b997-146">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="7b997-147">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7b997-147">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


