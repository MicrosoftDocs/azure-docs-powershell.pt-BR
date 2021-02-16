---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 4dceb934f5cf746908c289c7662de0dc3dae09a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113614"
---
# <span data-ttu-id="ee4d2-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ee4d2-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="ee4d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee4d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ee4d2-103">Remove uma montagem de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="ee4d2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee4d2-104">SYNTAX</span></span>

### <span data-ttu-id="ee4d2-105">ByIntegrationAccount (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ee4d2-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee4d2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ee4d2-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee4d2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ee4d2-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee4d2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee4d2-108">DESCRIPTION</span></span>
<span data-ttu-id="ee4d2-109">O cmdlet **Remove-AzIntegrationAccountAssembly** remove um assembly de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="ee4d2-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ee4d2-110">EXAMPLES</span></span>

### <span data-ttu-id="ee4d2-111">Exemplo 1: Remover um assembly por parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee4d2-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="ee4d2-112">Remove a montagem denominada "sampleAssembly" localizada na conta de integração "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="ee4d2-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="ee4d2-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee4d2-113">PARAMETERS</span></span>

### <span data-ttu-id="ee4d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee4d2-114">-DefaultProfile</span></span>
<span data-ttu-id="ee4d2-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee4d2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee4d2-116">-InputObject</span></span>
<span data-ttu-id="ee4d2-117">Uma montagem de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-117">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee4d2-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee4d2-118">-Name</span></span>
<span data-ttu-id="ee4d2-119">O nome de montagem da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4d2-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="ee4d2-120">-ParentName</span></span>
<span data-ttu-id="ee4d2-121">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4d2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee4d2-122">-PassThru</span></span>
<span data-ttu-id="ee4d2-123">Retorne se o comando foi bem-sucedido ou não.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-123">Return whether the command was successful or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee4d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="ee4d2-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4d2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee4d2-126">-ResourceId</span></span>
<span data-ttu-id="ee4d2-127">A ID do recurso de montagem de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-127">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee4d2-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ee4d2-128">-Confirm</span></span>
<span data-ttu-id="ee4d2-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee4d2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee4d2-130">-WhatIf</span></span>
<span data-ttu-id="ee4d2-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee4d2-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee4d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee4d2-133">CommonParameters</span></span>
<span data-ttu-id="ee4d2-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee4d2-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee4d2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee4d2-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="ee4d2-136">INPUTS</span></span>

### <span data-ttu-id="ee4d2-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ee4d2-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="ee4d2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ee4d2-138">System.String</span></span>

## <span data-ttu-id="ee4d2-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="ee4d2-139">OUTPUTS</span></span>

### <span data-ttu-id="ee4d2-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ee4d2-140">System.Boolean</span></span>

## <span data-ttu-id="ee4d2-141">Notas</span><span class="sxs-lookup"><span data-stu-id="ee4d2-141">NOTES</span></span>

## <span data-ttu-id="ee4d2-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee4d2-142">RELATED LINKS</span></span>
