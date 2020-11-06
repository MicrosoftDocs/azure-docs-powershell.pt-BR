---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: a87c75058e3ebfb1ae7d14e729fdc9280cdccb9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595701"
---
# <span data-ttu-id="ade77-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ade77-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="ade77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ade77-102">SYNOPSIS</span></span>
<span data-ttu-id="ade77-103">Obtém uma API.</span><span class="sxs-lookup"><span data-stu-id="ade77-103">Gets an API.</span></span>

## <span data-ttu-id="ade77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ade77-104">SYNTAX</span></span>

### <span data-ttu-id="ade77-105">GetAllApis (padrão)</span><span class="sxs-lookup"><span data-stu-id="ade77-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ade77-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="ade77-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ade77-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="ade77-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ade77-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="ade77-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ade77-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ade77-109">DESCRIPTION</span></span>
<span data-ttu-id="ade77-110">O cmdlet **Get-AzApiManagementApi** Obtém uma ou mais APIs de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="ade77-110">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="ade77-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ade77-111">EXAMPLES</span></span>

### <span data-ttu-id="ade77-112">Exemplo 1: obter todas as APIs de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="ade77-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="ade77-113">Esse comando obtém todas as APIs do contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="ade77-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="ade77-114">Exemplo 2: obter uma API de gerenciamento por ID</span><span class="sxs-lookup"><span data-stu-id="ade77-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="ade77-115">Este comando obtém a API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="ade77-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="ade77-116">Exemplo 3: obter uma API de gerenciamento por nome</span><span class="sxs-lookup"><span data-stu-id="ade77-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="ade77-117">Este comando obtém a API com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="ade77-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="ade77-118">OS</span><span class="sxs-lookup"><span data-stu-id="ade77-118">PARAMETERS</span></span>

### <span data-ttu-id="ade77-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ade77-119">-ApiId</span></span>
<span data-ttu-id="ade77-120">Especifica a ID da API a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="ade77-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade77-121">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="ade77-121">-ApiRevision</span></span>
<span data-ttu-id="ade77-122">Identificador de revisão da revisão da API específica.</span><span class="sxs-lookup"><span data-stu-id="ade77-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="ade77-123">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ade77-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade77-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ade77-124">-Context</span></span>
<span data-ttu-id="ade77-125">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ade77-125">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ade77-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade77-126">-DefaultProfile</span></span>
<span data-ttu-id="ade77-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ade77-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ade77-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="ade77-128">-Name</span></span>
<span data-ttu-id="ade77-129">Especifica o nome da API a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="ade77-129">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade77-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="ade77-130">-ProductId</span></span>
<span data-ttu-id="ade77-131">Especifica a ID do produto para o qual obter a API.</span><span class="sxs-lookup"><span data-stu-id="ade77-131">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade77-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade77-132">CommonParameters</span></span>
<span data-ttu-id="ade77-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ade77-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade77-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ade77-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade77-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ade77-135">INPUTS</span></span>

### <span data-ttu-id="ade77-136">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ade77-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ade77-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ade77-137">System.String</span></span>

## <span data-ttu-id="ade77-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ade77-138">OUTPUTS</span></span>

### <span data-ttu-id="ade77-139">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ade77-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="ade77-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ade77-140">NOTES</span></span>

## <span data-ttu-id="ade77-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ade77-141">RELATED LINKS</span></span>

[<span data-ttu-id="ade77-142">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ade77-142">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="ade77-143">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ade77-143">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="ade77-144">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ade77-144">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="ade77-145">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ade77-145">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="ade77-146">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ade77-146">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


