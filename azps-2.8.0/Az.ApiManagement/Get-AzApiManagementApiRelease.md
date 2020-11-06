---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 19395960d3a0026b7a14c4ca8232c18d511af989
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598127"
---
# <span data-ttu-id="eb6cb-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="eb6cb-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="eb6cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb6cb-102">SYNOPSIS</span></span>
<span data-ttu-id="eb6cb-103">Obtenha a versão da API.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-103">Get the API Release.</span></span>

## <span data-ttu-id="eb6cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb6cb-104">SYNTAX</span></span>

### <span data-ttu-id="eb6cb-105">ContextParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="eb6cb-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb6cb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb6cb-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb6cb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb6cb-107">DESCRIPTION</span></span>
<span data-ttu-id="eb6cb-108">O cmdlet **Get-AzApiManagementApiRelease** Obtém uma ou mais versões da API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="eb6cb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb6cb-109">EXAMPLES</span></span>

### <span data-ttu-id="eb6cb-110">Exemplo 1: obter todas as versões da API</span><span class="sxs-lookup"><span data-stu-id="eb6cb-110">Example 1: Get all releases of the API</span></span>
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

<span data-ttu-id="eb6cb-111">Esse comando obtém todas as versões da API do `echo-api` contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="eb6cb-112">Exemplo 2: obter as informações de versão do lançamento da API específica</span><span class="sxs-lookup"><span data-stu-id="eb6cb-112">Example 2: Get the release information of the particular API release</span></span>
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

<span data-ttu-id="eb6cb-113">Esse comando obtém as informações de versões de uma determinada API com o releaseid especificado.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="eb6cb-114">OS</span><span class="sxs-lookup"><span data-stu-id="eb6cb-114">PARAMETERS</span></span>

### <span data-ttu-id="eb6cb-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="eb6cb-115">-ApiId</span></span>
<span data-ttu-id="eb6cb-116">Identificador de API a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-116">API identifier to look for.</span></span>
<span data-ttu-id="eb6cb-117">Se especificado, você tentará obter a API pela ID.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="eb6cb-118">-Contexto</span><span class="sxs-lookup"><span data-stu-id="eb6cb-118">-Context</span></span>
<span data-ttu-id="eb6cb-119">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="eb6cb-120">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-120">This parameter is required.</span></span>

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

### <span data-ttu-id="eb6cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb6cb-121">-DefaultProfile</span></span>
<span data-ttu-id="eb6cb-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb6cb-123">-Rereleaseid</span><span class="sxs-lookup"><span data-stu-id="eb6cb-123">-ReleaseId</span></span>
<span data-ttu-id="eb6cb-124">O identificador do lançamento.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-124">The identifier of the Release.</span></span>

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

### <span data-ttu-id="eb6cb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb6cb-125">-ResourceId</span></span>
<span data-ttu-id="eb6cb-126">Identificador de recursos ARM de uma versão de API.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="eb6cb-127">Se especificado, você tentará localizar a versão da API pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="eb6cb-128">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-128">This parameter is required.</span></span>

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

### <span data-ttu-id="eb6cb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb6cb-129">CommonParameters</span></span>
<span data-ttu-id="eb6cb-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb6cb-131">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb6cb-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb6cb-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb6cb-132">INPUTS</span></span>

### <span data-ttu-id="eb6cb-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="eb6cb-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="eb6cb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="eb6cb-134">System.String</span></span>

## <span data-ttu-id="eb6cb-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb6cb-135">OUTPUTS</span></span>

### <span data-ttu-id="eb6cb-136">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="eb6cb-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="eb6cb-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb6cb-137">NOTES</span></span>

## <span data-ttu-id="eb6cb-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb6cb-138">RELATED LINKS</span></span>

[<span data-ttu-id="eb6cb-139">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="eb6cb-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="eb6cb-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="eb6cb-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="eb6cb-141">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="eb6cb-141">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)