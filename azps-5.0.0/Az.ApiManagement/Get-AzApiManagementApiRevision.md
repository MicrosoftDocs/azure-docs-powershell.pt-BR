---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: 16c108d4f62d9bcc44176fce7ede9a7e56d98687
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282301"
---
# <span data-ttu-id="bc419-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="bc419-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="bc419-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc419-102">SYNOPSIS</span></span>
<span data-ttu-id="bc419-103">Obtém detalhes de todas as revisões de API de uma API</span><span class="sxs-lookup"><span data-stu-id="bc419-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="bc419-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc419-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc419-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc419-105">DESCRIPTION</span></span>
<span data-ttu-id="bc419-106">O cmdlet **Get-AzApiManagementApiRevision** Obtém os detalhes de todas as revisões de uma API</span><span class="sxs-lookup"><span data-stu-id="bc419-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="bc419-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc419-107">EXAMPLES</span></span>

### <span data-ttu-id="bc419-108">Exemplo 1: obter todas as revisões de API de uma API</span><span class="sxs-lookup"><span data-stu-id="bc419-108">Example 1: Get all API Revisions of an API</span></span>
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

<span data-ttu-id="bc419-109">Esse comando obtém toda a versão da API especificada para o contexto ApiManagement específico.</span><span class="sxs-lookup"><span data-stu-id="bc419-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="bc419-110">OS</span><span class="sxs-lookup"><span data-stu-id="bc419-110">PARAMETERS</span></span>

### <span data-ttu-id="bc419-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bc419-111">-ApiId</span></span>
<span data-ttu-id="bc419-112">Identificador de API cujas revisões queremos listar.</span><span class="sxs-lookup"><span data-stu-id="bc419-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="bc419-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="bc419-113">This parameter is required.</span></span>

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

### <span data-ttu-id="bc419-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="bc419-114">-ApiRevision</span></span>
<span data-ttu-id="bc419-115">Identificador de revisão da revisão da API específica.</span><span class="sxs-lookup"><span data-stu-id="bc419-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="bc419-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="bc419-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="bc419-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="bc419-117">-Context</span></span>
<span data-ttu-id="bc419-118">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bc419-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bc419-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="bc419-119">This parameter is required.</span></span>

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

### <span data-ttu-id="bc419-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc419-120">-DefaultProfile</span></span>
<span data-ttu-id="bc419-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc419-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc419-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc419-122">CommonParameters</span></span>
<span data-ttu-id="bc419-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc419-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc419-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc419-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc419-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc419-125">INPUTS</span></span>

### <span data-ttu-id="bc419-126">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bc419-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bc419-127">System. String</span><span class="sxs-lookup"><span data-stu-id="bc419-127">System.String</span></span>

## <span data-ttu-id="bc419-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc419-128">OUTPUTS</span></span>

### <span data-ttu-id="bc419-129">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="bc419-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="bc419-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc419-130">NOTES</span></span>

## <span data-ttu-id="bc419-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc419-131">RELATED LINKS</span></span>
