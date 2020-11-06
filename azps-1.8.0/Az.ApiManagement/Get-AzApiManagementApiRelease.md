---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 353fd6365f85ba71105f80324ba740b4d829a85a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595699"
---
# <span data-ttu-id="90076-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="90076-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="90076-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90076-102">SYNOPSIS</span></span>
<span data-ttu-id="90076-103">Obtenha a versão da API.</span><span class="sxs-lookup"><span data-stu-id="90076-103">Get the API Release.</span></span>

## <span data-ttu-id="90076-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90076-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90076-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90076-105">DESCRIPTION</span></span>
<span data-ttu-id="90076-106">O cmdlet **Get-AzApiManagementApiRelease** Obtém uma ou mais versões da API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="90076-106">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="90076-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90076-107">EXAMPLES</span></span>

### <span data-ttu-id="90076-108">Exemplo 1: obter todas as versões da API</span><span class="sxs-lookup"><span data-stu-id="90076-108">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="90076-109">Esse comando obtém todas as versões da API do `echo-api` contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="90076-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="90076-110">Exemplo 2: obter as informações de versão do lançamento da API específica</span><span class="sxs-lookup"><span data-stu-id="90076-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
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

<span data-ttu-id="90076-111">Esse comando obtém as informações de versões de uma determinada API com o releaseid especificado.</span><span class="sxs-lookup"><span data-stu-id="90076-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="90076-112">OS</span><span class="sxs-lookup"><span data-stu-id="90076-112">PARAMETERS</span></span>

### <span data-ttu-id="90076-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="90076-113">-ApiId</span></span>
<span data-ttu-id="90076-114">Identificador de API a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="90076-114">API identifier to look for.</span></span>
<span data-ttu-id="90076-115">Se especificado, você tentará obter a API pela ID.</span><span class="sxs-lookup"><span data-stu-id="90076-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="90076-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="90076-116">-Context</span></span>
<span data-ttu-id="90076-117">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="90076-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="90076-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="90076-118">This parameter is required.</span></span>

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

### <span data-ttu-id="90076-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90076-119">-DefaultProfile</span></span>
<span data-ttu-id="90076-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90076-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90076-121">-Rereleaseid</span><span class="sxs-lookup"><span data-stu-id="90076-121">-ReleaseId</span></span>
<span data-ttu-id="90076-122">O identificador do lançamento.</span><span class="sxs-lookup"><span data-stu-id="90076-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="90076-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90076-123">CommonParameters</span></span>
<span data-ttu-id="90076-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90076-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90076-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90076-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90076-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90076-126">INPUTS</span></span>

### <span data-ttu-id="90076-127">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="90076-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="90076-128">System. String</span><span class="sxs-lookup"><span data-stu-id="90076-128">System.String</span></span>

## <span data-ttu-id="90076-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90076-129">OUTPUTS</span></span>

### <span data-ttu-id="90076-130">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="90076-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="90076-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90076-131">NOTES</span></span>

## <span data-ttu-id="90076-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90076-132">RELATED LINKS</span></span>

[<span data-ttu-id="90076-133">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="90076-133">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="90076-134">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="90076-134">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="90076-135">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="90076-135">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)