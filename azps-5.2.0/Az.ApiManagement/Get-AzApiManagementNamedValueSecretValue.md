---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263458"
---
# <span data-ttu-id="153c2-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="153c2-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="153c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="153c2-102">SYNOPSIS</span></span>
<span data-ttu-id="153c2-103">Obtém um valor secreto do valor nomeado específico.</span><span class="sxs-lookup"><span data-stu-id="153c2-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="153c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="153c2-104">SYNTAX</span></span>

### <span data-ttu-id="153c2-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="153c2-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="153c2-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="153c2-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="153c2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="153c2-107">DESCRIPTION</span></span>
<span data-ttu-id="153c2-108">Obtém um valor secreto do valor nomeado específico.</span><span class="sxs-lookup"><span data-stu-id="153c2-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="153c2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="153c2-109">EXAMPLES</span></span>

### <span data-ttu-id="153c2-110">Exemplo 1: obter valor nomeado por nome</span><span class="sxs-lookup"><span data-stu-id="153c2-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="153c2-111">Esse comando obtém os detalhes do valor nomeado de acordo com o nome do valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="153c2-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="153c2-112">OS</span><span class="sxs-lookup"><span data-stu-id="153c2-112">PARAMETERS</span></span>

### <span data-ttu-id="153c2-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="153c2-113">-Context</span></span>
<span data-ttu-id="153c2-114">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="153c2-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="153c2-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="153c2-115">This parameter is required.</span></span>

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

### <span data-ttu-id="153c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="153c2-116">-DefaultProfile</span></span>
<span data-ttu-id="153c2-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="153c2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="153c2-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="153c2-118">-NamedValueId</span></span>
<span data-ttu-id="153c2-119">Identificador de um valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="153c2-119">Identifier of a the named value.</span></span>
<span data-ttu-id="153c2-120">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="153c2-120">This parameter is required.</span></span>

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

### <span data-ttu-id="153c2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="153c2-121">CommonParameters</span></span>
<span data-ttu-id="153c2-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="153c2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="153c2-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="153c2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="153c2-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="153c2-124">INPUTS</span></span>

### <span data-ttu-id="153c2-125">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="153c2-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="153c2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="153c2-126">System.String</span></span>

## <span data-ttu-id="153c2-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="153c2-127">OUTPUTS</span></span>

### <span data-ttu-id="153c2-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="153c2-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="153c2-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="153c2-129">NOTES</span></span>

## <span data-ttu-id="153c2-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="153c2-130">RELATED LINKS</span></span>
