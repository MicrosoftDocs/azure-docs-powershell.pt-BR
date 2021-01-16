---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432718"
---
# <span data-ttu-id="896ae-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="896ae-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="896ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="896ae-102">SYNOPSIS</span></span>
<span data-ttu-id="896ae-103">Obtém uma lista ou um determinado valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="896ae-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="896ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="896ae-104">SYNTAX</span></span>

### <span data-ttu-id="896ae-105">GetAllNamedValues (padrão)</span><span class="sxs-lookup"><span data-stu-id="896ae-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="896ae-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="896ae-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="896ae-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="896ae-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="896ae-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="896ae-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="896ae-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="896ae-109">DESCRIPTION</span></span>
<span data-ttu-id="896ae-110">O cmdlet **Get-AzApiManagementNamedValue** Obtém uma lista ou um determinado valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="896ae-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="896ae-111">O valor não será incluído nos detalhes do resultado se o valor nomeado estiver marcado como um segredo.</span><span class="sxs-lookup"><span data-stu-id="896ae-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="896ae-112">Para obter valor secreto, use **Get-AzApiManagementNamedValueSecretValue**.</span><span class="sxs-lookup"><span data-stu-id="896ae-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="896ae-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="896ae-113">EXAMPLES</span></span>

### <span data-ttu-id="896ae-114">Exemplo 1: obter valor nomeado por nome</span><span class="sxs-lookup"><span data-stu-id="896ae-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="896ae-115">Esse comando obtém os detalhes do valor nomeado de acordo com o nome do valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="896ae-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="896ae-116">OS</span><span class="sxs-lookup"><span data-stu-id="896ae-116">PARAMETERS</span></span>

### <span data-ttu-id="896ae-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="896ae-117">-Context</span></span>
<span data-ttu-id="896ae-118">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="896ae-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="896ae-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="896ae-119">This parameter is required.</span></span>

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

### <span data-ttu-id="896ae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="896ae-120">-DefaultProfile</span></span>
<span data-ttu-id="896ae-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="896ae-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="896ae-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="896ae-122">-Name</span></span>
<span data-ttu-id="896ae-123">Localiza valores nomeados com nomes que contêm o nome da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="896ae-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="896ae-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="896ae-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="896ae-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="896ae-125">-NamedValueId</span></span>
<span data-ttu-id="896ae-126">Identificador do valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="896ae-126">Identifier of the named value.</span></span>
<span data-ttu-id="896ae-127">Se especificado, tentará localizar o valor nomeado pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="896ae-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="896ae-128">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="896ae-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="896ae-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="896ae-129">-Tag</span></span>
<span data-ttu-id="896ae-130">Localiza valores nomeados associados a uma marca.</span><span class="sxs-lookup"><span data-stu-id="896ae-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="896ae-131">Se especificado, retornará todas as propriedades associadas a uma marca.</span><span class="sxs-lookup"><span data-stu-id="896ae-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="896ae-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="896ae-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="896ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="896ae-133">CommonParameters</span></span>
<span data-ttu-id="896ae-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="896ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="896ae-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="896ae-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="896ae-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="896ae-136">INPUTS</span></span>

### <span data-ttu-id="896ae-137">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="896ae-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="896ae-138">System. String</span><span class="sxs-lookup"><span data-stu-id="896ae-138">System.String</span></span>

## <span data-ttu-id="896ae-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="896ae-139">OUTPUTS</span></span>

### <span data-ttu-id="896ae-140">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="896ae-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="896ae-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="896ae-141">NOTES</span></span>

## <span data-ttu-id="896ae-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="896ae-142">RELATED LINKS</span></span>
