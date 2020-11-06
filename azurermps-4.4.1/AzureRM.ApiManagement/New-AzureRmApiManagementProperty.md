---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: cb50ea5735a9f63f5f35b8f1cb0648c566e6108d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610227"
---
# <span data-ttu-id="3e3cf-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="3e3cf-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="3e3cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e3cf-102">SYNOPSIS</span></span>
<span data-ttu-id="3e3cf-103">Cria uma nova propriedade.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e3cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e3cf-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tags <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e3cf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e3cf-105">DESCRIPTION</span></span>
<span data-ttu-id="3e3cf-106">O cmdlet **New-AzureRmApiManagementProperty** cria uma **Propriedade** de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="3e3cf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e3cf-107">EXAMPLES</span></span>

### <span data-ttu-id="3e3cf-108">Exemplo 1: criar uma propriedade que inclua marcas</span><span class="sxs-lookup"><span data-stu-id="3e3cf-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="3e3cf-109">O primeiro comando atribui dois valores à variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="3e3cf-110">O segundo comando cria uma propriedade e atribui as cadeias de caracteres em $Tags como marcas na propriedade.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="3e3cf-111">Exemplo 2: criar uma propriedade com um valor secreto</span><span class="sxs-lookup"><span data-stu-id="3e3cf-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="3e3cf-112">Esse comando cria uma **Propriedade** que tem um valor criptografado.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="3e3cf-113">OS</span><span class="sxs-lookup"><span data-stu-id="3e3cf-113">PARAMETERS</span></span>

### <span data-ttu-id="3e3cf-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3e3cf-114">-Context</span></span>
<span data-ttu-id="3e3cf-115">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3e3cf-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3e3cf-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e3cf-116">-Name</span></span>
<span data-ttu-id="3e3cf-117">Especifica o nome da propriedade que esse cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-117">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="3e3cf-118">O comprimento máximo é de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-118">Maximum length is 100 characters.</span></span>
<span data-ttu-id="3e3cf-119">Os nomes contêm apenas letras, dígitos, ponto, traço e sublinhado caracteres.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-119">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="3e3cf-120">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="3e3cf-120">-PropertyId</span></span>
<span data-ttu-id="3e3cf-121">Especifica uma ID para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-121">Specifies an ID for the property.</span></span>
<span data-ttu-id="3e3cf-122">O comprimento máximo é de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-122">Maximum length is 256 characters.</span></span>
<span data-ttu-id="3e3cf-123">Se você não especificar uma ID, esse cmdlet gerará uma.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-123">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="3e3cf-124">-Segredo</span><span class="sxs-lookup"><span data-stu-id="3e3cf-124">-Secret</span></span>
<span data-ttu-id="3e3cf-125">Indica que o valor da propriedade é um segredo e deve ser criptografado.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-125">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="3e3cf-126">-Marcas</span><span class="sxs-lookup"><span data-stu-id="3e3cf-126">-Tags</span></span>
<span data-ttu-id="3e3cf-127">Especifica uma matriz de marcas que este cmdlet associa à propriedade.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-127">Specifies an array of tags that this cmdlet associates to the property.</span></span>
<span data-ttu-id="3e3cf-128">Você pode usar marcas para filtrar a lista de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-128">You can use tags to filter the property list.</span></span>

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

### <span data-ttu-id="3e3cf-129">-Valor</span><span class="sxs-lookup"><span data-stu-id="3e3cf-129">-Value</span></span>
<span data-ttu-id="3e3cf-130">Especifica um valor para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-130">Specifies a value for the property.</span></span>
<span data-ttu-id="3e3cf-131">Esse valor pode conter expressões de política.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-131">This value can contain policy expressions.</span></span>
<span data-ttu-id="3e3cf-132">O comprimento máximo é de 1000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-132">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="3e3cf-133">O valor não pode estar vazio ou consistir apenas em um espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-133">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="3e3cf-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e3cf-134">-DefaultProfile</span></span>
<span data-ttu-id="3e3cf-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e3cf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e3cf-136">CommonParameters</span></span>
<span data-ttu-id="3e3cf-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e3cf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e3cf-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e3cf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e3cf-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e3cf-139">INPUTS</span></span>

## <span data-ttu-id="3e3cf-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e3cf-140">OUTPUTS</span></span>

### <span data-ttu-id="3e3cf-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="3e3cf-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="3e3cf-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e3cf-142">NOTES</span></span>

## <span data-ttu-id="3e3cf-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e3cf-143">RELATED LINKS</span></span>

[<span data-ttu-id="3e3cf-144">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="3e3cf-144">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="3e3cf-145">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="3e3cf-145">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


