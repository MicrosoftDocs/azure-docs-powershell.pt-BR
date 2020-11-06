---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: 2ee3954569067000d445ecd7dab034db41734829
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428650"
---
# <span data-ttu-id="12baa-101">New-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="12baa-101">New-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="12baa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12baa-102">SYNOPSIS</span></span>
<span data-ttu-id="12baa-103">Cria uma nova revisão de uma API existente.</span><span class="sxs-lookup"><span data-stu-id="12baa-103">Creates a new Revision of an Existing API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12baa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12baa-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12baa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12baa-105">DESCRIPTION</span></span>

<span data-ttu-id="12baa-106">O cmdlet **New-AzureRmApiManagementApiRevision** cria uma revisão de API para uma API existente no contexto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="12baa-106">The **New-AzureRmApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="12baa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12baa-107">EXAMPLES</span></span>

### <span data-ttu-id="12baa-108">Exemplo 1: criar uma revisão de API para uma API</span><span class="sxs-lookup"><span data-stu-id="12baa-108">Example 1: Create an API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApiRevision -Context $ApiMgmtContext  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6


ApiId                         : 5adf6fbf0faadf3ad8558065;rev=6
Name                          : httpbin.org
Description                   : API Management facade for a very handy and free online HTTP tool.
ServiceUrl                    : https://httpbin.org/
Path                          : httpbin
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         : contoso-oauth
AuthorizationScope            : contoso-oauth
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 6
ApiVersion                    : v1
IsCurrent                     : False
IsOnline                      : False
Id                            : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065;rev=6
ResourceGroupName             : Api-Default-WestUS
ServiceName                   : contoso
```

<span data-ttu-id="12baa-109">Esse comando cria uma revisão `2` de API da `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="12baa-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

## <span data-ttu-id="12baa-110">OS</span><span class="sxs-lookup"><span data-stu-id="12baa-110">PARAMETERS</span></span>

### <span data-ttu-id="12baa-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="12baa-111">-ApiId</span></span>
<span data-ttu-id="12baa-112">Identificador de API cuja revisão será criada.</span><span class="sxs-lookup"><span data-stu-id="12baa-112">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="12baa-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="12baa-113">-ApiRevision</span></span>
<span data-ttu-id="12baa-114">Identificador de revisão da API.</span><span class="sxs-lookup"><span data-stu-id="12baa-114">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="12baa-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="12baa-115">-Context</span></span>
<span data-ttu-id="12baa-116">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="12baa-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="12baa-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="12baa-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12baa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12baa-118">-DefaultProfile</span></span>
<span data-ttu-id="12baa-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12baa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12baa-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12baa-120">-Confirm</span></span>
<span data-ttu-id="12baa-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12baa-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12baa-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12baa-122">-WhatIf</span></span>
<span data-ttu-id="12baa-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12baa-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12baa-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12baa-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12baa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12baa-125">CommonParameters</span></span>
<span data-ttu-id="12baa-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12baa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12baa-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12baa-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12baa-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12baa-128">INPUTS</span></span>

### <span data-ttu-id="12baa-129">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="12baa-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="12baa-130">Parâmetros: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="12baa-130">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="12baa-131">System. String</span><span class="sxs-lookup"><span data-stu-id="12baa-131">System.String</span></span>

## <span data-ttu-id="12baa-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12baa-132">OUTPUTS</span></span>

### <span data-ttu-id="12baa-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="12baa-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="12baa-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12baa-134">NOTES</span></span>

## <span data-ttu-id="12baa-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12baa-135">RELATED LINKS</span></span>

[<span data-ttu-id="12baa-136">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="12baa-136">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="12baa-137">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="12baa-137">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="12baa-138">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="12baa-138">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)
