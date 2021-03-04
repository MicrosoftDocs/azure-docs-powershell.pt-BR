---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ad0c40e649384d4fb2bef9220f6ab8a994dea96c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893257"
---
# <span data-ttu-id="b4943-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4943-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="b4943-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4943-102">SYNOPSIS</span></span>
<span data-ttu-id="b4943-103">Remove uma configuração de nome de host do Gateway existente.</span><span class="sxs-lookup"><span data-stu-id="b4943-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="b4943-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b4943-104">SYNTAX</span></span>

### <span data-ttu-id="b4943-105">ContextParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b4943-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4943-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4943-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4943-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4943-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4943-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b4943-108">DESCRIPTION</span></span>
<span data-ttu-id="b4943-109">O cmdlet **Remove-AzApiManagementGatewayHostnameConfiguration** remove uma configuração de nome de host do Gateway existente.</span><span class="sxs-lookup"><span data-stu-id="b4943-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="b4943-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4943-110">EXAMPLES</span></span>

### <span data-ttu-id="b4943-111">Exemplo 1: Remover uma configuração de nome de host de gateway existente</span><span class="sxs-lookup"><span data-stu-id="b4943-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="b4943-112">Este comando remove uma configuração de nome de host de gateway existente e não solicita confirmação ao usuário.</span><span class="sxs-lookup"><span data-stu-id="b4943-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="b4943-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b4943-113">PARAMETERS</span></span>

### <span data-ttu-id="b4943-114">-Context</span><span class="sxs-lookup"><span data-stu-id="b4943-114">-Context</span></span>
<span data-ttu-id="b4943-115">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b4943-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b4943-116">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b4943-116">This parameter is required.</span></span>

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

### <span data-ttu-id="b4943-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4943-117">-DefaultProfile</span></span>
<span data-ttu-id="b4943-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4943-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4943-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b4943-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="b4943-120">Identificador da configuração de nome de host do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="b4943-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="b4943-121">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b4943-121">This parameter is required.</span></span>

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

### <span data-ttu-id="b4943-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="b4943-122">-GatewayId</span></span>
<span data-ttu-id="b4943-123">Identificador do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="b4943-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="b4943-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b4943-124">This parameter is required.</span></span>

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

### <span data-ttu-id="b4943-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4943-125">-InputObject</span></span>
<span data-ttu-id="b4943-126">Instância de PsApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b4943-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="b4943-127">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b4943-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4943-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4943-128">-PassThru</span></span>
<span data-ttu-id="b4943-129">Se especificado, a gravação será true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b4943-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b4943-130">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b4943-130">This parameter is optional.</span></span>
<span data-ttu-id="b4943-131">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="b4943-131">Default value is false.</span></span>

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

### <span data-ttu-id="b4943-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4943-132">-ResourceId</span></span>
<span data-ttu-id="b4943-133">Arm ResourceId do GatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b4943-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="b4943-134">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b4943-134">This parameter is required.</span></span>

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

### <span data-ttu-id="b4943-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4943-135">-Confirm</span></span>
<span data-ttu-id="b4943-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4943-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4943-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4943-137">-WhatIf</span></span>
<span data-ttu-id="b4943-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4943-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4943-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4943-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4943-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4943-140">CommonParameters</span></span>
<span data-ttu-id="b4943-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4943-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4943-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4943-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4943-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4943-143">INPUTS</span></span>

### <span data-ttu-id="b4943-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b4943-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b4943-145">System.String</span><span class="sxs-lookup"><span data-stu-id="b4943-145">System.String</span></span>

### <span data-ttu-id="b4943-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b4943-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b4943-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b4943-147">OUTPUTS</span></span>

### <span data-ttu-id="b4943-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4943-148">System.Boolean</span></span>

## <span data-ttu-id="b4943-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="b4943-149">NOTES</span></span>

## <span data-ttu-id="b4943-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4943-150">RELATED LINKS</span></span>
