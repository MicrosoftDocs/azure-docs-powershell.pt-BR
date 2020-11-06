---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: f57a95e97c0ec74e7e45338e15a028feab60849b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431478"
---
# <span data-ttu-id="6a04e-101">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6a04e-101">Get-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="6a04e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a04e-102">SYNOPSIS</span></span>
<span data-ttu-id="6a04e-103">Obtém detalhes de todas as revisões de API de uma API</span><span class="sxs-lookup"><span data-stu-id="6a04e-103">Gets details of all the API Revisions of an API</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a04e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a04e-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a04e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6a04e-105">DESCRIPTION</span></span>
<span data-ttu-id="6a04e-106">O cmdlet **Get-AzureRmApiManagementApiRevision** Obtém os detalhes de todas as revisões de uma API</span><span class="sxs-lookup"><span data-stu-id="6a04e-106">The **Get-AzureRmApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="6a04e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a04e-107">EXAMPLES</span></span>

### <span data-ttu-id="6a04e-108">Exemplo 1: obter todas as revisões de API de uma API</span><span class="sxs-lookup"><span data-stu-id="6a04e-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=3
ApiRevision     : 3
CreatedDateTime : 4/26/2018 10:57:42 PM
UpdatedDateTime : 4/26/2018 10:57:42 PM
Description     : ddsds
PrivateUrl      : /httpbin/v1;rev=3
IsOnline        : True
IsCurrent       : False

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=2
ApiRevision     : 2
CreatedDateTime : 4/26/2018 10:57:33 PM
UpdatedDateTime : 4/26/2018 10:57:33 PM
Description     : AA
PrivateUrl      : /httpbin/v1
IsOnline        : True
IsCurrent       : True

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=1
ApiRevision     : 1
CreatedDateTime : 4/24/2018 5:56:17 PM
UpdatedDateTime : 5/9/2018 9:29:06 PM
Description     :
PrivateUrl      : /httpbin/v1;rev=1
IsOnline        : True
IsCurrent       : False
```

<span data-ttu-id="6a04e-109">Esse comando obtém toda a versão da API especificada para o contexto ApiManagement específico.</span><span class="sxs-lookup"><span data-stu-id="6a04e-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="6a04e-110">OS</span><span class="sxs-lookup"><span data-stu-id="6a04e-110">PARAMETERS</span></span>

### <span data-ttu-id="6a04e-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6a04e-111">-ApiId</span></span>
<span data-ttu-id="6a04e-112">Identificador de API cujas revisões queremos listar.</span><span class="sxs-lookup"><span data-stu-id="6a04e-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="6a04e-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6a04e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="6a04e-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="6a04e-114">-ApiRevision</span></span>
<span data-ttu-id="6a04e-115">Identificador de revisão da revisão da API específica.</span><span class="sxs-lookup"><span data-stu-id="6a04e-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="6a04e-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="6a04e-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="6a04e-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="6a04e-117">-Context</span></span>
<span data-ttu-id="6a04e-118">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6a04e-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6a04e-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6a04e-119">This parameter is required.</span></span>

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

### <span data-ttu-id="6a04e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a04e-120">-DefaultProfile</span></span>
<span data-ttu-id="6a04e-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a04e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a04e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a04e-122">CommonParameters</span></span>
<span data-ttu-id="6a04e-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a04e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a04e-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a04e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a04e-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6a04e-125">INPUTS</span></span>

### <span data-ttu-id="6a04e-126">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6a04e-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6a04e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6a04e-127">System.String</span></span>

## <span data-ttu-id="6a04e-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6a04e-128">OUTPUTS</span></span>

### <span data-ttu-id="6a04e-129">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6a04e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="6a04e-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6a04e-130">NOTES</span></span>

## <span data-ttu-id="6a04e-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a04e-131">RELATED LINKS</span></span>
