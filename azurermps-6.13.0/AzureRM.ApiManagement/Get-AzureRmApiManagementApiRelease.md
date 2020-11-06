---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 880d96ba0e9eff053084517452c03ffb018b72a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602128"
---
# <span data-ttu-id="65d20-101">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="65d20-101">Get-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="65d20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65d20-102">SYNOPSIS</span></span>
<span data-ttu-id="65d20-103">Obtenha a versão da API.</span><span class="sxs-lookup"><span data-stu-id="65d20-103">Get the API Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65d20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65d20-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65d20-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65d20-105">DESCRIPTION</span></span>
<span data-ttu-id="65d20-106">O cmdlet **Get-AzureRmApiManagementApiRelease** Obtém uma ou mais versões da API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="65d20-106">The **Get-AzureRmApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="65d20-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65d20-107">EXAMPLES</span></span>

### <span data-ttu-id="65d20-108">Exemplo 1: obter todas as versões da API</span><span class="sxs-lookup"><span data-stu-id="65d20-108">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="65d20-109">Esse comando obtém todas as versões da API do `echo-api` contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="65d20-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="65d20-110">Exemplo 2: obter as informações de versão do lançamento da API específica</span><span class="sxs-lookup"><span data-stu-id="65d20-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contos/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="65d20-111">Esse comando obtém as informações de versões de uma determinada API com o releaseid especificado.</span><span class="sxs-lookup"><span data-stu-id="65d20-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="65d20-112">OS</span><span class="sxs-lookup"><span data-stu-id="65d20-112">PARAMETERS</span></span>

### <span data-ttu-id="65d20-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="65d20-113">-ApiId</span></span>
<span data-ttu-id="65d20-114">Identificador de API a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="65d20-114">API identifier to look for.</span></span>
<span data-ttu-id="65d20-115">Se especificado, você tentará obter a API pela ID.</span><span class="sxs-lookup"><span data-stu-id="65d20-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="65d20-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="65d20-116">-Context</span></span>
<span data-ttu-id="65d20-117">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="65d20-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="65d20-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="65d20-118">This parameter is required.</span></span>

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

### <span data-ttu-id="65d20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d20-119">-DefaultProfile</span></span>
<span data-ttu-id="65d20-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65d20-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d20-121">-Rereleaseid</span><span class="sxs-lookup"><span data-stu-id="65d20-121">-ReleaseId</span></span>
<span data-ttu-id="65d20-122">O identificador do lançamento.</span><span class="sxs-lookup"><span data-stu-id="65d20-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="65d20-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d20-123">CommonParameters</span></span>
<span data-ttu-id="65d20-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65d20-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d20-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65d20-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d20-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65d20-126">INPUTS</span></span>

### <span data-ttu-id="65d20-127">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="65d20-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="65d20-128">System. String</span><span class="sxs-lookup"><span data-stu-id="65d20-128">System.String</span></span>

## <span data-ttu-id="65d20-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65d20-129">OUTPUTS</span></span>

### <span data-ttu-id="65d20-130">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="65d20-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="65d20-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65d20-131">NOTES</span></span>

## <span data-ttu-id="65d20-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65d20-132">RELATED LINKS</span></span>

[<span data-ttu-id="65d20-133">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="65d20-133">New-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="65d20-134">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="65d20-134">Remove-AzureRmApiManagementApiRelease</span></span>](./Remove-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="65d20-135">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="65d20-135">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
