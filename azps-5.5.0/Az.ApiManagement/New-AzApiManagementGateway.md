---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: c06442ef9ab4b5f80943da33ed87fc24c276107d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115567"
---
# <span data-ttu-id="e33b6-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="e33b6-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="e33b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e33b6-102">SYNOPSIS</span></span>
<span data-ttu-id="e33b6-103">Cria uma nova entidade gateway.</span><span class="sxs-lookup"><span data-stu-id="e33b6-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="e33b6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e33b6-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e33b6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e33b6-105">DESCRIPTION</span></span>
<span data-ttu-id="e33b6-106">O cmdlet **New-AzApiManagementGateway** cria uma nova entidade gateway.</span><span class="sxs-lookup"><span data-stu-id="e33b6-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="e33b6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e33b6-107">EXAMPLES</span></span>

### <span data-ttu-id="e33b6-108">Exemplo 1: Criar um gateway</span><span class="sxs-lookup"><span data-stu-id="e33b6-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="e33b6-109">Esse comando cria um gateway.</span><span class="sxs-lookup"><span data-stu-id="e33b6-109">This command creates a gateway.</span></span>

## <span data-ttu-id="e33b6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e33b6-110">PARAMETERS</span></span>

### <span data-ttu-id="e33b6-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e33b6-111">-Context</span></span>
<span data-ttu-id="e33b6-112">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e33b6-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e33b6-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e33b6-113">This parameter is required.</span></span>

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

### <span data-ttu-id="e33b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e33b6-114">-DefaultProfile</span></span>
<span data-ttu-id="e33b6-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e33b6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e33b6-116">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e33b6-116">-Description</span></span>
<span data-ttu-id="e33b6-117">Descrição do gateway.</span><span class="sxs-lookup"><span data-stu-id="e33b6-117">Gateway description.</span></span>
<span data-ttu-id="e33b6-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e33b6-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="e33b6-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e33b6-119">-GatewayId</span></span>
<span data-ttu-id="e33b6-120">Identificador do novo gateway.</span><span class="sxs-lookup"><span data-stu-id="e33b6-120">Identifier of new gateway.</span></span>
<span data-ttu-id="e33b6-121">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e33b6-121">This parameter is optional.</span></span>
<span data-ttu-id="e33b6-122">Se não especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="e33b6-122">If not specified will be generated.</span></span>

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

### <span data-ttu-id="e33b6-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="e33b6-123">-LocationData</span></span>
<span data-ttu-id="e33b6-124">Local do gateway.</span><span class="sxs-lookup"><span data-stu-id="e33b6-124">Gateway location.</span></span>
<span data-ttu-id="e33b6-125">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e33b6-125">This parameter is required.</span></span>

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

### <span data-ttu-id="e33b6-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e33b6-126">-Confirm</span></span>
<span data-ttu-id="e33b6-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e33b6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e33b6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e33b6-128">-WhatIf</span></span>
<span data-ttu-id="e33b6-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e33b6-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e33b6-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e33b6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e33b6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e33b6-131">CommonParameters</span></span>
<span data-ttu-id="e33b6-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e33b6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e33b6-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e33b6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e33b6-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="e33b6-134">INPUTS</span></span>

### <span data-ttu-id="e33b6-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e33b6-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e33b6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e33b6-136">System.String</span></span>

### <span data-ttu-id="e33b6-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="e33b6-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="e33b6-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="e33b6-138">OUTPUTS</span></span>

### <span data-ttu-id="e33b6-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="e33b6-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="e33b6-140">Notas</span><span class="sxs-lookup"><span data-stu-id="e33b6-140">NOTES</span></span>

## <span data-ttu-id="e33b6-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e33b6-141">RELATED LINKS</span></span>
