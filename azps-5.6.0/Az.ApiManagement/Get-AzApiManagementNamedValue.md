---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 791bbe35b480fe9779712d33a37a999bb651a132
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887605"
---
# <span data-ttu-id="29ae8-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="29ae8-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="29ae8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="29ae8-103">Obtém uma lista ou um valor nomeado específico.</span><span class="sxs-lookup"><span data-stu-id="29ae8-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="29ae8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="29ae8-104">SYNTAX</span></span>

### <span data-ttu-id="29ae8-105">GetAllNamedValues (Padrão)</span><span class="sxs-lookup"><span data-stu-id="29ae8-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29ae8-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="29ae8-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29ae8-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="29ae8-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29ae8-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="29ae8-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29ae8-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="29ae8-109">DESCRIPTION</span></span>
<span data-ttu-id="29ae8-110">O cmdlet **Get-AzApiManagementNamedValue** obtém uma lista ou um determinado valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="29ae8-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="29ae8-111">O valor não será incluído em detalhes do resultado se o valor nomeado marcado como um segredo.</span><span class="sxs-lookup"><span data-stu-id="29ae8-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="29ae8-112">Para obter valor secreto, use **Get-AzApiManagementNamedValueSecretValue**.</span><span class="sxs-lookup"><span data-stu-id="29ae8-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="29ae8-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29ae8-113">EXAMPLES</span></span>

### <span data-ttu-id="29ae8-114">Exemplo 1: Obter Valor Nomeado pelo nome</span><span class="sxs-lookup"><span data-stu-id="29ae8-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="29ae8-115">Este comando obtém os detalhes de valor nomeados com o nome do valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="29ae8-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="29ae8-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="29ae8-116">PARAMETERS</span></span>

### <span data-ttu-id="29ae8-117">-Context</span><span class="sxs-lookup"><span data-stu-id="29ae8-117">-Context</span></span>
<span data-ttu-id="29ae8-118">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="29ae8-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="29ae8-119">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="29ae8-119">This parameter is required.</span></span>

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

### <span data-ttu-id="29ae8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ae8-120">-DefaultProfile</span></span>
<span data-ttu-id="29ae8-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29ae8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29ae8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="29ae8-122">-Name</span></span>
<span data-ttu-id="29ae8-123">Localiza valores nomeados com nomes que contêm a cadeia de caracteres Name.</span><span class="sxs-lookup"><span data-stu-id="29ae8-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="29ae8-124">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="29ae8-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ae8-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="29ae8-125">-NamedValueId</span></span>
<span data-ttu-id="29ae8-126">Identificador do valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="29ae8-126">Identifier of the named value.</span></span>
<span data-ttu-id="29ae8-127">Se especificado, tentará encontrar o valor nomeado pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="29ae8-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="29ae8-128">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="29ae8-128">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ae8-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="29ae8-129">-Tag</span></span>
<span data-ttu-id="29ae8-130">Localiza valores nomeados associados a uma Marca.</span><span class="sxs-lookup"><span data-stu-id="29ae8-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="29ae8-131">Se especificado, retornará todas as propriedades associadas a uma marca.</span><span class="sxs-lookup"><span data-stu-id="29ae8-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="29ae8-132">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="29ae8-132">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ae8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ae8-133">CommonParameters</span></span>
<span data-ttu-id="29ae8-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29ae8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ae8-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29ae8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ae8-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29ae8-136">INPUTS</span></span>

### <span data-ttu-id="29ae8-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="29ae8-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="29ae8-138">System.String</span><span class="sxs-lookup"><span data-stu-id="29ae8-138">System.String</span></span>

## <span data-ttu-id="29ae8-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="29ae8-139">OUTPUTS</span></span>

### <span data-ttu-id="29ae8-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="29ae8-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="29ae8-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="29ae8-141">NOTES</span></span>

## <span data-ttu-id="29ae8-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29ae8-142">RELATED LINKS</span></span>
