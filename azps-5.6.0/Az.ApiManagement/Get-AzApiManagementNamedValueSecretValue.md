---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 1ef17239338319696d08a316648a158039fa63f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888337"
---
# <span data-ttu-id="a3986-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="a3986-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="a3986-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3986-102">SYNOPSIS</span></span>
<span data-ttu-id="a3986-103">Obtém um valor secreto do valor nomeado específico.</span><span class="sxs-lookup"><span data-stu-id="a3986-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="a3986-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a3986-104">SYNTAX</span></span>

### <span data-ttu-id="a3986-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a3986-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3986-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="a3986-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3986-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a3986-107">DESCRIPTION</span></span>
<span data-ttu-id="a3986-108">Obtém um valor secreto do valor nomeado específico.</span><span class="sxs-lookup"><span data-stu-id="a3986-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="a3986-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3986-109">EXAMPLES</span></span>

### <span data-ttu-id="a3986-110">Exemplo 1: Obter o valor nomeado por nome</span><span class="sxs-lookup"><span data-stu-id="a3986-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="a3986-111">Este comando obtém os detalhes de valor nomeados com o nome do valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="a3986-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="a3986-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a3986-112">PARAMETERS</span></span>

### <span data-ttu-id="a3986-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a3986-113">-Context</span></span>
<span data-ttu-id="a3986-114">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a3986-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a3986-115">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="a3986-115">This parameter is required.</span></span>

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

### <span data-ttu-id="a3986-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3986-116">-DefaultProfile</span></span>
<span data-ttu-id="a3986-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3986-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3986-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="a3986-118">-NamedValueId</span></span>
<span data-ttu-id="a3986-119">Identificador de um valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="a3986-119">Identifier of a the named value.</span></span>
<span data-ttu-id="a3986-120">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="a3986-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3986-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3986-121">CommonParameters</span></span>
<span data-ttu-id="a3986-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3986-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3986-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3986-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3986-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3986-124">INPUTS</span></span>

### <span data-ttu-id="a3986-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a3986-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a3986-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a3986-126">System.String</span></span>

## <span data-ttu-id="a3986-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a3986-127">OUTPUTS</span></span>

### <span data-ttu-id="a3986-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="a3986-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="a3986-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="a3986-129">NOTES</span></span>

## <span data-ttu-id="a3986-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3986-130">RELATED LINKS</span></span>
