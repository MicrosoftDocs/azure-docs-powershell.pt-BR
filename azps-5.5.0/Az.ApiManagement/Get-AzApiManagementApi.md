---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 8b6f27191ee92240a8dc9e5e8289fda72db856ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110846"
---
# <span data-ttu-id="17df7-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="17df7-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="17df7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17df7-102">SYNOPSIS</span></span>
<span data-ttu-id="17df7-103">Obtém uma API.</span><span class="sxs-lookup"><span data-stu-id="17df7-103">Gets an API.</span></span>

## <span data-ttu-id="17df7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17df7-104">SYNTAX</span></span>

### <span data-ttu-id="17df7-105">GetAllApis (Padrão)</span><span class="sxs-lookup"><span data-stu-id="17df7-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17df7-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="17df7-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17df7-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="17df7-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17df7-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="17df7-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17df7-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="17df7-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17df7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="17df7-110">DESCRIPTION</span></span>
<span data-ttu-id="17df7-111">O cmdlet **Get-AzApiManagementApi** obtém uma ou mais APIs de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="17df7-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="17df7-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="17df7-112">EXAMPLES</span></span>

### <span data-ttu-id="17df7-113">Exemplo 1: Obter todas as APIs de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="17df7-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="17df7-114">Esse comando obtém todas as APIs para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="17df7-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="17df7-115">Exemplo 2: Obter uma API de gerenciamento por ID</span><span class="sxs-lookup"><span data-stu-id="17df7-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="17df7-116">Esse comando obtém a API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="17df7-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="17df7-117">Exemplo 3: Obter uma API de gerenciamento por nome</span><span class="sxs-lookup"><span data-stu-id="17df7-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="17df7-118">Esse comando obtém a API com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="17df7-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="17df7-119">Exemplo 4: Obter uma API de gerenciamento pelo GatewayId</span><span class="sxs-lookup"><span data-stu-id="17df7-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="17df7-120">Esse comando obtém a API para o GatewayId especificado.</span><span class="sxs-lookup"><span data-stu-id="17df7-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="17df7-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17df7-121">PARAMETERS</span></span>

### <span data-ttu-id="17df7-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="17df7-122">-ApiId</span></span>
<span data-ttu-id="17df7-123">Especifica a ID da API a ser usada.</span><span class="sxs-lookup"><span data-stu-id="17df7-123">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="17df7-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="17df7-124">-ApiRevision</span></span>
<span data-ttu-id="17df7-125">Identificador de Revisão da revisão de Api específica.</span><span class="sxs-lookup"><span data-stu-id="17df7-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="17df7-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="17df7-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="17df7-127">-Contexto</span><span class="sxs-lookup"><span data-stu-id="17df7-127">-Context</span></span>
<span data-ttu-id="17df7-128">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="17df7-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="17df7-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17df7-129">-DefaultProfile</span></span>
<span data-ttu-id="17df7-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="17df7-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17df7-131">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="17df7-131">-GatewayId</span></span>
<span data-ttu-id="17df7-132">Se especificado, você tentará obter todas as APIs do Gateway.</span><span class="sxs-lookup"><span data-stu-id="17df7-132">If specified will try to get all Gateway APIs.</span></span>

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

### <span data-ttu-id="17df7-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="17df7-133">-Name</span></span>
<span data-ttu-id="17df7-134">Especifica o nome da API a ser usada.</span><span class="sxs-lookup"><span data-stu-id="17df7-134">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="17df7-135">-ProductId</span><span class="sxs-lookup"><span data-stu-id="17df7-135">-ProductId</span></span>
<span data-ttu-id="17df7-136">Especifica a ID do produto para o qual obter a API.</span><span class="sxs-lookup"><span data-stu-id="17df7-136">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="17df7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17df7-137">CommonParameters</span></span>
<span data-ttu-id="17df7-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17df7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17df7-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17df7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17df7-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="17df7-140">INPUTS</span></span>

### <span data-ttu-id="17df7-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="17df7-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="17df7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="17df7-142">System.String</span></span>

## <span data-ttu-id="17df7-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="17df7-143">OUTPUTS</span></span>

### <span data-ttu-id="17df7-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="17df7-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="17df7-145">Notas</span><span class="sxs-lookup"><span data-stu-id="17df7-145">NOTES</span></span>

## <span data-ttu-id="17df7-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17df7-146">RELATED LINKS</span></span>

[<span data-ttu-id="17df7-147">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="17df7-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="17df7-148">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="17df7-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="17df7-149">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="17df7-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="17df7-150">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="17df7-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="17df7-151">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="17df7-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


