---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: bb27324c2c8524f36d9f3362dee8968fbfb0cc8c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409776"
---
# <span data-ttu-id="b8196-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b8196-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="b8196-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8196-102">SYNOPSIS</span></span>
<span data-ttu-id="b8196-103">Obter o Lançamento da API.</span><span class="sxs-lookup"><span data-stu-id="b8196-103">Get the API Release.</span></span>

## <span data-ttu-id="b8196-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8196-104">SYNTAX</span></span>

### <span data-ttu-id="b8196-105">ContextParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b8196-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8196-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8196-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8196-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8196-107">DESCRIPTION</span></span>
<span data-ttu-id="b8196-108">O cmdlet **Get-AzApiManagementApiRelease** recebe uma ou mais versões da API de Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="b8196-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="b8196-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b8196-109">EXAMPLES</span></span>

### <span data-ttu-id="b8196-110">Exemplo 1: Obter todas as versões da API</span><span class="sxs-lookup"><span data-stu-id="b8196-110">Example 1: Get all releases of the API</span></span>
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

<span data-ttu-id="b8196-111">Esse comando obtém todas as versões da `echo-api` API para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="b8196-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="b8196-112">Exemplo 2: Obter as informações de versão da versão específica da API</span><span class="sxs-lookup"><span data-stu-id="b8196-112">Example 2: Get the release information of the particular API release</span></span>
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

<span data-ttu-id="b8196-113">Esse comando obtém as informações de versões de uma API específica com o releaseId especificado.</span><span class="sxs-lookup"><span data-stu-id="b8196-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="b8196-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8196-114">PARAMETERS</span></span>

### <span data-ttu-id="b8196-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b8196-115">-ApiId</span></span>
<span data-ttu-id="b8196-116">Identificador de API a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="b8196-116">API identifier to look for.</span></span>
<span data-ttu-id="b8196-117">Se especificado, você tentará obter a API pela ID.</span><span class="sxs-lookup"><span data-stu-id="b8196-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="b8196-118">-Contexto</span><span class="sxs-lookup"><span data-stu-id="b8196-118">-Context</span></span>
<span data-ttu-id="b8196-119">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b8196-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b8196-120">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b8196-120">This parameter is required.</span></span>

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

### <span data-ttu-id="b8196-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8196-121">-DefaultProfile</span></span>
<span data-ttu-id="b8196-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8196-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8196-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="b8196-123">-ReleaseId</span></span>
<span data-ttu-id="b8196-124">O identificador do Lançamento.</span><span class="sxs-lookup"><span data-stu-id="b8196-124">The identifier of the Release.</span></span>

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

### <span data-ttu-id="b8196-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8196-125">-ResourceId</span></span>
<span data-ttu-id="b8196-126">Identificador de Recursos Arm de uma Versão da Api.</span><span class="sxs-lookup"><span data-stu-id="b8196-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="b8196-127">Se especificado, tentará encontrar a versão da api pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="b8196-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="b8196-128">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b8196-128">This parameter is required.</span></span>

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

### <span data-ttu-id="b8196-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8196-129">CommonParameters</span></span>
<span data-ttu-id="b8196-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8196-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8196-131">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8196-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8196-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="b8196-132">INPUTS</span></span>

### <span data-ttu-id="b8196-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b8196-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b8196-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b8196-134">System.String</span></span>

## <span data-ttu-id="b8196-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="b8196-135">OUTPUTS</span></span>

### <span data-ttu-id="b8196-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b8196-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="b8196-137">Notas</span><span class="sxs-lookup"><span data-stu-id="b8196-137">NOTES</span></span>

## <span data-ttu-id="b8196-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8196-138">RELATED LINKS</span></span>

[<span data-ttu-id="b8196-139">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b8196-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="b8196-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b8196-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="b8196-141">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b8196-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)