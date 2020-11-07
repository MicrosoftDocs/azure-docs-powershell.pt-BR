---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
ms.openlocfilehash: d54665b767d10edde564450ecfcdd467b784dd8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771413"
---
# <span data-ttu-id="6403d-101">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="6403d-101">New-AzApiManagementProperty</span></span>

## <span data-ttu-id="6403d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6403d-102">SYNOPSIS</span></span>
<span data-ttu-id="6403d-103">Cria uma nova propriedade.</span><span class="sxs-lookup"><span data-stu-id="6403d-103">Creates a new Property.</span></span>

## <span data-ttu-id="6403d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6403d-104">SYNTAX</span></span>

```
New-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6403d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6403d-105">DESCRIPTION</span></span>
<span data-ttu-id="6403d-106">O cmdlet **New-AzApiManagementProperty** cria uma **Propriedade** de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="6403d-106">The **New-AzApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="6403d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6403d-107">EXAMPLES</span></span>

### <span data-ttu-id="6403d-108">Exemplo 1: criar uma propriedade que inclua marcas</span><span class="sxs-lookup"><span data-stu-id="6403d-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="6403d-109">O primeiro comando atribui dois valores à variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="6403d-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="6403d-110">O segundo comando cria uma propriedade e atribui as cadeias de caracteres em $Tags como marcas na propriedade.</span><span class="sxs-lookup"><span data-stu-id="6403d-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="6403d-111">Exemplo 2: criar uma propriedade com um valor secreto</span><span class="sxs-lookup"><span data-stu-id="6403d-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="6403d-112">Esse comando cria uma **Propriedade** que tem um valor criptografado.</span><span class="sxs-lookup"><span data-stu-id="6403d-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="6403d-113">OS</span><span class="sxs-lookup"><span data-stu-id="6403d-113">PARAMETERS</span></span>

### <span data-ttu-id="6403d-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="6403d-114">-Context</span></span>
<span data-ttu-id="6403d-115">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6403d-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6403d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6403d-116">-DefaultProfile</span></span>
<span data-ttu-id="6403d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6403d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6403d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6403d-118">-Name</span></span>
<span data-ttu-id="6403d-119">Especifica o nome da propriedade que esse cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="6403d-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="6403d-120">O comprimento máximo é de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6403d-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="6403d-121">Os nomes contêm apenas letras, dígitos, ponto, traço e sublinhado caracteres.</span><span class="sxs-lookup"><span data-stu-id="6403d-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="6403d-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="6403d-122">-PropertyId</span></span>
<span data-ttu-id="6403d-123">Especifica uma ID para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="6403d-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="6403d-124">O comprimento máximo é de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6403d-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="6403d-125">Se você não especificar uma ID, esse cmdlet gerará uma.</span><span class="sxs-lookup"><span data-stu-id="6403d-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="6403d-126">-Segredo</span><span class="sxs-lookup"><span data-stu-id="6403d-126">-Secret</span></span>
<span data-ttu-id="6403d-127">Indica que o valor da propriedade é um segredo e deve ser criptografado.</span><span class="sxs-lookup"><span data-stu-id="6403d-127">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="6403d-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="6403d-128">-Tag</span></span>
<span data-ttu-id="6403d-129">Marcas a serem associadas à propriedade.</span><span class="sxs-lookup"><span data-stu-id="6403d-129">Tags to be associated with Property.</span></span> <span data-ttu-id="6403d-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="6403d-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="6403d-131">-Valor</span><span class="sxs-lookup"><span data-stu-id="6403d-131">-Value</span></span>
<span data-ttu-id="6403d-132">Especifica um valor para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="6403d-132">Specifies a value for the property.</span></span>
<span data-ttu-id="6403d-133">Esse valor pode conter expressões de política.</span><span class="sxs-lookup"><span data-stu-id="6403d-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="6403d-134">O comprimento máximo é de 1000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6403d-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="6403d-135">O valor não pode estar vazio ou consistir apenas em um espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="6403d-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="6403d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6403d-136">CommonParameters</span></span>
<span data-ttu-id="6403d-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6403d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6403d-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6403d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6403d-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6403d-139">INPUTS</span></span>

### <span data-ttu-id="6403d-140">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6403d-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6403d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6403d-141">System.String</span></span>

### <span data-ttu-id="6403d-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6403d-142">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6403d-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="6403d-143">System.String[]</span></span>

## <span data-ttu-id="6403d-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6403d-144">OUTPUTS</span></span>

### <span data-ttu-id="6403d-145">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="6403d-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="6403d-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6403d-146">NOTES</span></span>

## <span data-ttu-id="6403d-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6403d-147">RELATED LINKS</span></span>

[<span data-ttu-id="6403d-148">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="6403d-148">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)

[<span data-ttu-id="6403d-149">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="6403d-149">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


