---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 2ccd68fb5c1028408771e3011642797c8125ace3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890883"
---
# <span data-ttu-id="53eac-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="53eac-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="53eac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53eac-102">SYNOPSIS</span></span>
<span data-ttu-id="53eac-103">Desconecta uma API de um Gateway.</span><span class="sxs-lookup"><span data-stu-id="53eac-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="53eac-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="53eac-104">SYNTAX</span></span>

### <span data-ttu-id="53eac-105">ContextParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="53eac-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53eac-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53eac-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53eac-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53eac-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53eac-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="53eac-108">DESCRIPTION</span></span>
<span data-ttu-id="53eac-109">O cmdlet **Remove-AzApiManagementGateway** desconecta uma API de um Gateway.</span><span class="sxs-lookup"><span data-stu-id="53eac-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="53eac-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53eac-110">EXAMPLES</span></span>

### <span data-ttu-id="53eac-111">Exemplo 1: Remover um gateway existente</span><span class="sxs-lookup"><span data-stu-id="53eac-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="53eac-112">Este comando remove um gateway existente e não solicita a confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="53eac-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="53eac-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="53eac-113">PARAMETERS</span></span>

### <span data-ttu-id="53eac-114">-Context</span><span class="sxs-lookup"><span data-stu-id="53eac-114">-Context</span></span>
<span data-ttu-id="53eac-115">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="53eac-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="53eac-116">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="53eac-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53eac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53eac-117">-DefaultProfile</span></span>
<span data-ttu-id="53eac-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53eac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53eac-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="53eac-119">-GatewayId</span></span>
<span data-ttu-id="53eac-120">Identificador do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="53eac-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="53eac-121">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="53eac-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53eac-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53eac-122">-InputObject</span></span>
<span data-ttu-id="53eac-123">Instância de PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="53eac-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="53eac-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="53eac-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53eac-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53eac-125">-PassThru</span></span>
<span data-ttu-id="53eac-126">Se especificado, a gravação será true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="53eac-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="53eac-127">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="53eac-127">This parameter is optional.</span></span>
<span data-ttu-id="53eac-128">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="53eac-128">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53eac-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53eac-129">-ResourceId</span></span>
<span data-ttu-id="53eac-130">Arm ResourceId do Gateway.</span><span class="sxs-lookup"><span data-stu-id="53eac-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="53eac-131">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="53eac-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53eac-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53eac-132">-Confirm</span></span>
<span data-ttu-id="53eac-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53eac-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53eac-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53eac-134">-WhatIf</span></span>
<span data-ttu-id="53eac-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53eac-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53eac-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53eac-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53eac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53eac-137">CommonParameters</span></span>
<span data-ttu-id="53eac-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53eac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53eac-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53eac-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53eac-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53eac-140">INPUTS</span></span>

### <span data-ttu-id="53eac-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="53eac-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="53eac-142">System.String</span><span class="sxs-lookup"><span data-stu-id="53eac-142">System.String</span></span>

### <span data-ttu-id="53eac-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="53eac-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="53eac-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="53eac-144">OUTPUTS</span></span>

### <span data-ttu-id="53eac-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="53eac-145">System.Boolean</span></span>

## <span data-ttu-id="53eac-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="53eac-146">NOTES</span></span>

## <span data-ttu-id="53eac-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53eac-147">RELATED LINKS</span></span>
