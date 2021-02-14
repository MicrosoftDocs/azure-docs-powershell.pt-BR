---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: e1999387cc2beb5a55fba3aef771a76440804f22
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111228"
---
# <span data-ttu-id="e03e6-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e03e6-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="e03e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e03e6-102">SYNOPSIS</span></span>
<span data-ttu-id="e03e6-103">Remove uma configuração de nome de host do Gateway existente.</span><span class="sxs-lookup"><span data-stu-id="e03e6-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="e03e6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e03e6-104">SYNTAX</span></span>

### <span data-ttu-id="e03e6-105">ContextParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e03e6-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e03e6-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e03e6-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e03e6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e03e6-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e03e6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e03e6-108">DESCRIPTION</span></span>
<span data-ttu-id="e03e6-109">O cmdlet **Remove-AzApiManagementGatewayHostnameConfiguration** remove uma configuração de nome de host do Gateway existente.</span><span class="sxs-lookup"><span data-stu-id="e03e6-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="e03e6-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e03e6-110">EXAMPLES</span></span>

### <span data-ttu-id="e03e6-111">Exemplo 1: Remover uma configuração de nome de host de gateway existente</span><span class="sxs-lookup"><span data-stu-id="e03e6-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="e03e6-112">Esse comando remove uma configuração de nome de host do gateway existente e não solicita confirmação ao usuário.</span><span class="sxs-lookup"><span data-stu-id="e03e6-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="e03e6-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e03e6-113">PARAMETERS</span></span>

### <span data-ttu-id="e03e6-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e03e6-114">-Context</span></span>
<span data-ttu-id="e03e6-115">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e03e6-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e03e6-116">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e03e6-116">This parameter is required.</span></span>

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

### <span data-ttu-id="e03e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e03e6-117">-DefaultProfile</span></span>
<span data-ttu-id="e03e6-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e03e6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e03e6-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e03e6-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="e03e6-120">Identificador de configuração de nome de host do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="e03e6-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="e03e6-121">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e03e6-121">This parameter is required.</span></span>

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

### <span data-ttu-id="e03e6-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e03e6-122">-GatewayId</span></span>
<span data-ttu-id="e03e6-123">Identificador do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="e03e6-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="e03e6-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e03e6-124">This parameter is required.</span></span>

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

### <span data-ttu-id="e03e6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e03e6-125">-InputObject</span></span>
<span data-ttu-id="e03e6-126">Instância de PsApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e03e6-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="e03e6-127">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e03e6-127">This parameter is required.</span></span>

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

### <span data-ttu-id="e03e6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e03e6-128">-PassThru</span></span>
<span data-ttu-id="e03e6-129">Se especificado, a gravação será verdadeira caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e03e6-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="e03e6-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e03e6-130">This parameter is optional.</span></span>
<span data-ttu-id="e03e6-131">O valor padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="e03e6-131">Default value is false.</span></span>

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

### <span data-ttu-id="e03e6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e03e6-132">-ResourceId</span></span>
<span data-ttu-id="e03e6-133">Arm ResourceId da GatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e03e6-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="e03e6-134">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e03e6-134">This parameter is required.</span></span>

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

### <span data-ttu-id="e03e6-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e03e6-135">-Confirm</span></span>
<span data-ttu-id="e03e6-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e03e6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e03e6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e03e6-137">-WhatIf</span></span>
<span data-ttu-id="e03e6-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e03e6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e03e6-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e03e6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e03e6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e03e6-140">CommonParameters</span></span>
<span data-ttu-id="e03e6-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e03e6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e03e6-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e03e6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e03e6-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="e03e6-143">INPUTS</span></span>

### <span data-ttu-id="e03e6-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e03e6-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e03e6-145">System.String</span><span class="sxs-lookup"><span data-stu-id="e03e6-145">System.String</span></span>

### <span data-ttu-id="e03e6-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e03e6-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e03e6-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="e03e6-147">OUTPUTS</span></span>

### <span data-ttu-id="e03e6-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e03e6-148">System.Boolean</span></span>

## <span data-ttu-id="e03e6-149">Notas</span><span class="sxs-lookup"><span data-stu-id="e03e6-149">NOTES</span></span>

## <span data-ttu-id="e03e6-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e03e6-150">RELATED LINKS</span></span>
