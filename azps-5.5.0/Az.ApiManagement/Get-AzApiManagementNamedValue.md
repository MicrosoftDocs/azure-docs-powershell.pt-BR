---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118068"
---
# <span data-ttu-id="25346-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="25346-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="25346-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25346-102">SYNOPSIS</span></span>
<span data-ttu-id="25346-103">Obtém uma lista ou um determinado Valor Nomeado.</span><span class="sxs-lookup"><span data-stu-id="25346-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="25346-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25346-104">SYNTAX</span></span>

### <span data-ttu-id="25346-105">GetAllNamedValues (Padrão)</span><span class="sxs-lookup"><span data-stu-id="25346-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25346-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="25346-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25346-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="25346-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25346-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="25346-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25346-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="25346-109">DESCRIPTION</span></span>
<span data-ttu-id="25346-110">O cmdlet **Get-AzApiManagementNamedValue** obtém uma lista ou um valor nomeado específico.</span><span class="sxs-lookup"><span data-stu-id="25346-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="25346-111">O valor não será incluído nos detalhes do resultado se o valor nomeado for marcado como um segredo.</span><span class="sxs-lookup"><span data-stu-id="25346-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="25346-112">Para obter um valor secreto, use **Get-AzApiManagementNamedValueSecvalue.**</span><span class="sxs-lookup"><span data-stu-id="25346-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="25346-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="25346-113">EXAMPLES</span></span>

### <span data-ttu-id="25346-114">Exemplo 1: Obter Valor Nomeado por nome</span><span class="sxs-lookup"><span data-stu-id="25346-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="25346-115">Esse comando obtém os detalhes do valor nomeado de acordo com o nome do valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="25346-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="25346-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25346-116">PARAMETERS</span></span>

### <span data-ttu-id="25346-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="25346-117">-Context</span></span>
<span data-ttu-id="25346-118">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="25346-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="25346-119">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="25346-119">This parameter is required.</span></span>

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

### <span data-ttu-id="25346-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25346-120">-DefaultProfile</span></span>
<span data-ttu-id="25346-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25346-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25346-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="25346-122">-Name</span></span>
<span data-ttu-id="25346-123">Localiza valores nomeados com nomes que contêm o Nome da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="25346-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="25346-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="25346-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="25346-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="25346-125">-NamedValueId</span></span>
<span data-ttu-id="25346-126">Identificador do valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="25346-126">Identifier of the named value.</span></span>
<span data-ttu-id="25346-127">Se especificado, tentará encontrar o valor nomeado pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="25346-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="25346-128">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="25346-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="25346-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="25346-129">-Tag</span></span>
<span data-ttu-id="25346-130">Localiza valores nomeados associados a uma Marca.</span><span class="sxs-lookup"><span data-stu-id="25346-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="25346-131">Se especificado, todas as propriedades associadas a uma marca serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="25346-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="25346-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="25346-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="25346-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25346-133">CommonParameters</span></span>
<span data-ttu-id="25346-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25346-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25346-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25346-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25346-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="25346-136">INPUTS</span></span>

### <span data-ttu-id="25346-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="25346-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="25346-138">System.String</span><span class="sxs-lookup"><span data-stu-id="25346-138">System.String</span></span>

## <span data-ttu-id="25346-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="25346-139">OUTPUTS</span></span>

### <span data-ttu-id="25346-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="25346-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="25346-141">Notas</span><span class="sxs-lookup"><span data-stu-id="25346-141">NOTES</span></span>

## <span data-ttu-id="25346-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25346-142">RELATED LINKS</span></span>
