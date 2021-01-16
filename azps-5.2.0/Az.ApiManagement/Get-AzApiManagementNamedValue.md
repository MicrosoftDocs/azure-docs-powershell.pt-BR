---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260913"
---
# <span data-ttu-id="e8e1c-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="e8e1c-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="e8e1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e1c-103">Obtém uma lista ou um determinado valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="e8e1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8e1c-104">SYNTAX</span></span>

### <span data-ttu-id="e8e1c-105">GetAllNamedValues (padrão)</span><span class="sxs-lookup"><span data-stu-id="e8e1c-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8e1c-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="e8e1c-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8e1c-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="e8e1c-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8e1c-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="e8e1c-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8e1c-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8e1c-109">DESCRIPTION</span></span>
<span data-ttu-id="e8e1c-110">O cmdlet **Get-AzApiManagementNamedValue** Obtém uma lista ou um determinado valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="e8e1c-111">O valor não será incluído nos detalhes do resultado se o valor nomeado estiver marcado como um segredo.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="e8e1c-112">Para obter valor secreto, use **Get-AzApiManagementNamedValueSecretValue**.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="e8e1c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8e1c-113">EXAMPLES</span></span>

### <span data-ttu-id="e8e1c-114">Exemplo 1: obter valor nomeado por nome</span><span class="sxs-lookup"><span data-stu-id="e8e1c-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="e8e1c-115">Esse comando obtém os detalhes do valor nomeado de acordo com o nome do valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="e8e1c-116">OS</span><span class="sxs-lookup"><span data-stu-id="e8e1c-116">PARAMETERS</span></span>

### <span data-ttu-id="e8e1c-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e8e1c-117">-Context</span></span>
<span data-ttu-id="e8e1c-118">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e8e1c-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-119">This parameter is required.</span></span>

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

### <span data-ttu-id="e8e1c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8e1c-120">-DefaultProfile</span></span>
<span data-ttu-id="e8e1c-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8e1c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8e1c-122">-Name</span></span>
<span data-ttu-id="e8e1c-123">Localiza valores nomeados com nomes que contêm o nome da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="e8e1c-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8e1c-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="e8e1c-125">-NamedValueId</span></span>
<span data-ttu-id="e8e1c-126">Identificador do valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-126">Identifier of the named value.</span></span>
<span data-ttu-id="e8e1c-127">Se especificado, tentará localizar o valor nomeado pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="e8e1c-128">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8e1c-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="e8e1c-129">-Tag</span></span>
<span data-ttu-id="e8e1c-130">Localiza valores nomeados associados a uma marca.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="e8e1c-131">Se especificado, retornará todas as propriedades associadas a uma marca.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="e8e1c-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8e1c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e1c-133">CommonParameters</span></span>
<span data-ttu-id="e8e1c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e1c-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8e1c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e1c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8e1c-136">INPUTS</span></span>

### <span data-ttu-id="e8e1c-137">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e8e1c-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e8e1c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e8e1c-138">System.String</span></span>

## <span data-ttu-id="e8e1c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8e1c-139">OUTPUTS</span></span>

### <span data-ttu-id="e8e1c-140">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="e8e1c-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="e8e1c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8e1c-141">NOTES</span></span>

## <span data-ttu-id="e8e1c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8e1c-142">RELATED LINKS</span></span>
