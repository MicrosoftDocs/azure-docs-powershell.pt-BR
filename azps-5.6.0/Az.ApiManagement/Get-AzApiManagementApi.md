---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 5e1cbec98e2b501a71f022766f7248c3209d590f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890486"
---
# <span data-ttu-id="c9bfd-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c9bfd-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="c9bfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="c9bfd-103">Obtém uma API.</span><span class="sxs-lookup"><span data-stu-id="c9bfd-103">Gets an API.</span></span>

## <span data-ttu-id="c9bfd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c9bfd-104">SYNTAX</span></span>

### <span data-ttu-id="c9bfd-105">GetAllApis (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c9bfd-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9bfd-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="c9bfd-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9bfd-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="c9bfd-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9bfd-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="c9bfd-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9bfd-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="c9bfd-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9bfd-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c9bfd-110">DESCRIPTION</span></span>
<span data-ttu-id="c9bfd-111">O cmdlet **Get-AzApiManagementApi** obtém uma ou mais APIs de Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="c9bfd-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="c9bfd-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9bfd-112">EXAMPLES</span></span>

### <span data-ttu-id="c9bfd-113">Exemplo 1: Obter todas as APIs de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="c9bfd-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="c9bfd-114">Este comando obtém todas as APIs do contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="c9bfd-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="c9bfd-115">Exemplo 2: Obter uma API de gerenciamento por ID</span><span class="sxs-lookup"><span data-stu-id="c9bfd-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="c9bfd-116">Esse comando obtém a API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="c9bfd-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="c9bfd-117">Exemplo 3: Obter uma API de gerenciamento pelo nome</span><span class="sxs-lookup"><span data-stu-id="c9bfd-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="c9bfd-118">Este comando obtém a API com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="c9bfd-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="c9bfd-119">Exemplo 4: Obter uma API de gerenciamento por GatewayId</span><span class="sxs-lookup"><span data-stu-id="c9bfd-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="c9bfd-120">Este comando obtém a API para o GatewayId especificado.</span><span class="sxs-lookup"><span data-stu-id="c9bfd-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="c9bfd-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c9bfd-121">PARAMETERS</span></span>

### <span data-ttu-id="c9bfd-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c9bfd-122">-ApiId</span></span>
<span data-ttu-id="c9bfd-123">Especifica a ID da API a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c9bfd-123">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="c9bfd-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c9bfd-124">-ApiRevision</span></span>
<span data-ttu-id="c9bfd-125">Identificador de revisão da revisão da Api específica.</span><span class="sxs-lookup"><span data-stu-id="c9bfd-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="c9bfd-126">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c9bfd-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="c9bfd-127">-Context</span><span class="sxs-lookup"><span data-stu-id="c9bfd-127">-Context</span></span>
<span data-ttu-id="c9bfd-128">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="c9bfd-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c9bfd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9bfd-129">-DefaultProfile</span></span>
<span data-ttu-id="c9bfd-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c9bfd-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9bfd-131">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="c9bfd-131">-GatewayId</span></span>
<span data-ttu-id="c9bfd-132">Se especificado, tentará obter todas as APIs do Gateway.</span><span class="sxs-lookup"><span data-stu-id="c9bfd-132">If specified will try to get all Gateway APIs.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9bfd-133">-Name</span><span class="sxs-lookup"><span data-stu-id="c9bfd-133">-Name</span></span>
<span data-ttu-id="c9bfd-134">Especifica o nome da API a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c9bfd-134">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="c9bfd-135">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c9bfd-135">-ProductId</span></span>
<span data-ttu-id="c9bfd-136">Especifica a ID do produto para o qual obter a API.</span><span class="sxs-lookup"><span data-stu-id="c9bfd-136">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="c9bfd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9bfd-137">CommonParameters</span></span>
<span data-ttu-id="c9bfd-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9bfd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9bfd-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9bfd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9bfd-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9bfd-140">INPUTS</span></span>

### <span data-ttu-id="c9bfd-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c9bfd-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c9bfd-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c9bfd-142">System.String</span></span>

## <span data-ttu-id="c9bfd-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c9bfd-143">OUTPUTS</span></span>

### <span data-ttu-id="c9bfd-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c9bfd-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="c9bfd-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="c9bfd-145">NOTES</span></span>

## <span data-ttu-id="c9bfd-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9bfd-146">RELATED LINKS</span></span>

[<span data-ttu-id="c9bfd-147">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c9bfd-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="c9bfd-148">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c9bfd-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="c9bfd-149">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c9bfd-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="c9bfd-150">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c9bfd-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="c9bfd-151">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c9bfd-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


