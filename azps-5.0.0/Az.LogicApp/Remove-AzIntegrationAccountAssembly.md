---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 4dceb934f5cf746908c289c7662de0dc3dae09a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126074"
---
# <span data-ttu-id="adb76-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="adb76-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="adb76-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="adb76-102">SYNOPSIS</span></span>
<span data-ttu-id="adb76-103">Remove um assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="adb76-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="adb76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="adb76-104">SYNTAX</span></span>

### <span data-ttu-id="adb76-105">ByIntegrationAccount (padrão)</span><span class="sxs-lookup"><span data-stu-id="adb76-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adb76-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="adb76-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adb76-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="adb76-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adb76-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="adb76-108">DESCRIPTION</span></span>
<span data-ttu-id="adb76-109">O cmdlet **Remove-AzIntegrationAccountAssembly** remove um assembly de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="adb76-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="adb76-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="adb76-110">EXAMPLES</span></span>

### <span data-ttu-id="adb76-111">Exemplo 1: remover um assembly por parâmetros</span><span class="sxs-lookup"><span data-stu-id="adb76-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="adb76-112">Remove o assembly chamado "sampleAssembly" localizado na conta de integração "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="adb76-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="adb76-113">OS</span><span class="sxs-lookup"><span data-stu-id="adb76-113">PARAMETERS</span></span>

### <span data-ttu-id="adb76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb76-114">-DefaultProfile</span></span>
<span data-ttu-id="adb76-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="adb76-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adb76-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adb76-116">-InputObject</span></span>
<span data-ttu-id="adb76-117">Um assembly de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="adb76-117">An integration account assembly.</span></span>

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

### <span data-ttu-id="adb76-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="adb76-118">-Name</span></span>
<span data-ttu-id="adb76-119">O nome do assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="adb76-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="adb76-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="adb76-120">-ParentName</span></span>
<span data-ttu-id="adb76-121">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="adb76-121">The integration account name.</span></span>

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

### <span data-ttu-id="adb76-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adb76-122">-PassThru</span></span>
<span data-ttu-id="adb76-123">Retorna se o comando foi bem-sucedido ou não.</span><span class="sxs-lookup"><span data-stu-id="adb76-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="adb76-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adb76-124">-ResourceGroupName</span></span>
<span data-ttu-id="adb76-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="adb76-125">The resource group name.</span></span>

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

### <span data-ttu-id="adb76-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adb76-126">-ResourceId</span></span>
<span data-ttu-id="adb76-127">A ID do recurso assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="adb76-127">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="adb76-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="adb76-128">-Confirm</span></span>
<span data-ttu-id="adb76-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adb76-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adb76-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adb76-130">-WhatIf</span></span>
<span data-ttu-id="adb76-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="adb76-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="adb76-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="adb76-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adb76-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb76-133">CommonParameters</span></span>
<span data-ttu-id="adb76-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adb76-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb76-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adb76-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb76-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="adb76-136">INPUTS</span></span>

### <span data-ttu-id="adb76-137">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="adb76-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="adb76-138">System. String</span><span class="sxs-lookup"><span data-stu-id="adb76-138">System.String</span></span>

## <span data-ttu-id="adb76-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="adb76-139">OUTPUTS</span></span>

### <span data-ttu-id="adb76-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="adb76-140">System.Boolean</span></span>

## <span data-ttu-id="adb76-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="adb76-141">NOTES</span></span>

## <span data-ttu-id="adb76-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adb76-142">RELATED LINKS</span></span>
