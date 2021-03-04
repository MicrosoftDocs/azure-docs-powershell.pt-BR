---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: e653053264baaa343b474f534f30915d725e5553
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890323"
---
# <span data-ttu-id="91115-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="91115-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="91115-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91115-102">SYNOPSIS</span></span>
<span data-ttu-id="91115-103">Obtém detalhes de todas as revisões de API de uma API</span><span class="sxs-lookup"><span data-stu-id="91115-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="91115-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="91115-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91115-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="91115-105">DESCRIPTION</span></span>
<span data-ttu-id="91115-106">O cmdlet **Get-AzApiManagementApiRevision** obtém os detalhes de todas as revisões de uma API</span><span class="sxs-lookup"><span data-stu-id="91115-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="91115-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91115-107">EXAMPLES</span></span>

### <span data-ttu-id="91115-108">Exemplo 1: Obter todas as revisões de API de uma API</span><span class="sxs-lookup"><span data-stu-id="91115-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

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

<span data-ttu-id="91115-109">Este comando obtém toda a revisão da API da API especificada para o Contexto de ApiManagement específico.</span><span class="sxs-lookup"><span data-stu-id="91115-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="91115-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="91115-110">PARAMETERS</span></span>

### <span data-ttu-id="91115-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="91115-111">-ApiId</span></span>
<span data-ttu-id="91115-112">Identificador de API cujas revisões queremos listar.</span><span class="sxs-lookup"><span data-stu-id="91115-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="91115-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="91115-113">This parameter is required.</span></span>

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

### <span data-ttu-id="91115-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="91115-114">-ApiRevision</span></span>
<span data-ttu-id="91115-115">Identificador de revisão da revisão da Api específica.</span><span class="sxs-lookup"><span data-stu-id="91115-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="91115-116">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="91115-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="91115-117">-Context</span><span class="sxs-lookup"><span data-stu-id="91115-117">-Context</span></span>
<span data-ttu-id="91115-118">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="91115-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="91115-119">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="91115-119">This parameter is required.</span></span>

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

### <span data-ttu-id="91115-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91115-120">-DefaultProfile</span></span>
<span data-ttu-id="91115-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91115-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91115-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91115-122">CommonParameters</span></span>
<span data-ttu-id="91115-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91115-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91115-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91115-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91115-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91115-125">INPUTS</span></span>

### <span data-ttu-id="91115-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="91115-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="91115-127">System.String</span><span class="sxs-lookup"><span data-stu-id="91115-127">System.String</span></span>

## <span data-ttu-id="91115-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="91115-128">OUTPUTS</span></span>

### <span data-ttu-id="91115-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="91115-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="91115-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="91115-130">NOTES</span></span>

## <span data-ttu-id="91115-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91115-131">RELATED LINKS</span></span>
