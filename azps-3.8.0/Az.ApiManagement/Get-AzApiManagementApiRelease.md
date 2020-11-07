---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: de4f91e7d2df778952ca505f37f1d6f6874a6524
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941954"
---
# <span data-ttu-id="33d05-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="33d05-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="33d05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33d05-102">SYNOPSIS</span></span>
<span data-ttu-id="33d05-103">Obtenha a versão da API.</span><span class="sxs-lookup"><span data-stu-id="33d05-103">Get the API Release.</span></span>

## <span data-ttu-id="33d05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33d05-104">SYNTAX</span></span>

### <span data-ttu-id="33d05-105">ContextParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="33d05-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33d05-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33d05-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33d05-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33d05-107">DESCRIPTION</span></span>
<span data-ttu-id="33d05-108">O cmdlet **Get-AzApiManagementApiRelease** Obtém uma ou mais versões da API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="33d05-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="33d05-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33d05-109">EXAMPLES</span></span>

### <span data-ttu-id="33d05-110">Exemplo 1: obter todas as versões da API</span><span class="sxs-lookup"><span data-stu-id="33d05-110">Example 1: Get all releases of the API</span></span>
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
ServiceName       : contoso
```

<span data-ttu-id="33d05-111">Esse comando obtém todas as versões da API do `echo-api` contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="33d05-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="33d05-112">Exemplo 2: obter as informações de versão do lançamento da API específica</span><span class="sxs-lookup"><span data-stu-id="33d05-112">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="33d05-113">Esse comando obtém as informações de versões de uma determinada API com o releaseid especificado.</span><span class="sxs-lookup"><span data-stu-id="33d05-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="33d05-114">OS</span><span class="sxs-lookup"><span data-stu-id="33d05-114">PARAMETERS</span></span>

### <span data-ttu-id="33d05-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="33d05-115">-ApiId</span></span>
<span data-ttu-id="33d05-116">Identificador de API a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="33d05-116">API identifier to look for.</span></span>
<span data-ttu-id="33d05-117">Se especificado, você tentará obter a API pela ID.</span><span class="sxs-lookup"><span data-stu-id="33d05-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33d05-118">-Contexto</span><span class="sxs-lookup"><span data-stu-id="33d05-118">-Context</span></span>
<span data-ttu-id="33d05-119">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="33d05-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="33d05-120">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="33d05-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33d05-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d05-121">-DefaultProfile</span></span>
<span data-ttu-id="33d05-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33d05-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33d05-123">-Rereleaseid</span><span class="sxs-lookup"><span data-stu-id="33d05-123">-ReleaseId</span></span>
<span data-ttu-id="33d05-124">O identificador do lançamento.</span><span class="sxs-lookup"><span data-stu-id="33d05-124">The identifier of the Release.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33d05-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33d05-125">-ResourceId</span></span>
<span data-ttu-id="33d05-126">Identificador de recursos ARM de uma versão de API.</span><span class="sxs-lookup"><span data-stu-id="33d05-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="33d05-127">Se especificado, você tentará localizar a versão da API pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="33d05-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="33d05-128">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="33d05-128">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33d05-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d05-129">CommonParameters</span></span>
<span data-ttu-id="33d05-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33d05-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d05-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33d05-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d05-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33d05-132">INPUTS</span></span>

### <span data-ttu-id="33d05-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="33d05-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="33d05-134">System. String</span><span class="sxs-lookup"><span data-stu-id="33d05-134">System.String</span></span>

## <span data-ttu-id="33d05-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33d05-135">OUTPUTS</span></span>

### <span data-ttu-id="33d05-136">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="33d05-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="33d05-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33d05-137">NOTES</span></span>

## <span data-ttu-id="33d05-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33d05-138">RELATED LINKS</span></span>

[<span data-ttu-id="33d05-139">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="33d05-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="33d05-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="33d05-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="33d05-141">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="33d05-141">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)