---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: 61a60949d88fd25c1205debb23aaed295122f376
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886369"
---
# <span data-ttu-id="384c7-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="384c7-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="384c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="384c7-102">SYNOPSIS</span></span>
<span data-ttu-id="384c7-103">Cria a nova entidade Gateway.</span><span class="sxs-lookup"><span data-stu-id="384c7-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="384c7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="384c7-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="384c7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="384c7-105">DESCRIPTION</span></span>
<span data-ttu-id="384c7-106">O cmdlet **New-AzApiManagementGateway** cria a nova entidade Gateway.</span><span class="sxs-lookup"><span data-stu-id="384c7-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="384c7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="384c7-107">EXAMPLES</span></span>

### <span data-ttu-id="384c7-108">Exemplo 1: Criar um gateway</span><span class="sxs-lookup"><span data-stu-id="384c7-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="384c7-109">Este comando cria um gateway.</span><span class="sxs-lookup"><span data-stu-id="384c7-109">This command creates a gateway.</span></span>

## <span data-ttu-id="384c7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="384c7-110">PARAMETERS</span></span>

### <span data-ttu-id="384c7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="384c7-111">-Context</span></span>
<span data-ttu-id="384c7-112">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="384c7-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="384c7-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="384c7-113">This parameter is required.</span></span>

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

### <span data-ttu-id="384c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="384c7-114">-DefaultProfile</span></span>
<span data-ttu-id="384c7-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="384c7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="384c7-116">-Description</span><span class="sxs-lookup"><span data-stu-id="384c7-116">-Description</span></span>
<span data-ttu-id="384c7-117">Descrição do gateway.</span><span class="sxs-lookup"><span data-stu-id="384c7-117">Gateway description.</span></span>
<span data-ttu-id="384c7-118">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="384c7-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="384c7-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="384c7-119">-GatewayId</span></span>
<span data-ttu-id="384c7-120">Identificador do novo gateway.</span><span class="sxs-lookup"><span data-stu-id="384c7-120">Identifier of new gateway.</span></span>
<span data-ttu-id="384c7-121">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="384c7-121">This parameter is optional.</span></span>
<span data-ttu-id="384c7-122">Se não for especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="384c7-122">If not specified will be generated.</span></span>

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

### <span data-ttu-id="384c7-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="384c7-123">-LocationData</span></span>
<span data-ttu-id="384c7-124">Local do gateway.</span><span class="sxs-lookup"><span data-stu-id="384c7-124">Gateway location.</span></span>
<span data-ttu-id="384c7-125">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="384c7-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="384c7-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="384c7-126">-Confirm</span></span>
<span data-ttu-id="384c7-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="384c7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="384c7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="384c7-128">-WhatIf</span></span>
<span data-ttu-id="384c7-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="384c7-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="384c7-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="384c7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="384c7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="384c7-131">CommonParameters</span></span>
<span data-ttu-id="384c7-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="384c7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="384c7-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="384c7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="384c7-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="384c7-134">INPUTS</span></span>

### <span data-ttu-id="384c7-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="384c7-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="384c7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="384c7-136">System.String</span></span>

### <span data-ttu-id="384c7-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="384c7-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="384c7-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="384c7-138">OUTPUTS</span></span>

### <span data-ttu-id="384c7-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="384c7-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="384c7-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="384c7-140">NOTES</span></span>

## <span data-ttu-id="384c7-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="384c7-141">RELATED LINKS</span></span>
