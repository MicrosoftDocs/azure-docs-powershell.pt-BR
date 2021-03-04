---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 4d153a05ad245eeece671adced6aa2f8029dc9a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892897"
---
# <span data-ttu-id="5e14f-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="5e14f-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="5e14f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e14f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e14f-103">Remove um tipo de conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="5e14f-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="5e14f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5e14f-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e14f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5e14f-105">DESCRIPTION</span></span>
<span data-ttu-id="5e14f-106">O cmdlet **Remove-AzAutomationConnectionType** remove um tipo de conexão da Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e14f-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="5e14f-107">Todas as conexões associadas ao tipo de conexão que você excluir se tornam inutilizáveis.</span><span class="sxs-lookup"><span data-stu-id="5e14f-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="5e14f-108">Remova-os, a menos que você crie um novo tipo de conexão que atenda aos seguintes critérios:</span><span class="sxs-lookup"><span data-stu-id="5e14f-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="5e14f-109">O tipo tem o mesmo nome do tipo de conexão original.</span><span class="sxs-lookup"><span data-stu-id="5e14f-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="5e14f-110">O tipo tem as mesmas definições de campo que o tipo de conexão original.</span><span class="sxs-lookup"><span data-stu-id="5e14f-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="5e14f-111">Ele pode ter campos adicionais.</span><span class="sxs-lookup"><span data-stu-id="5e14f-111">It can have additional fields.</span></span>

## <span data-ttu-id="5e14f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e14f-112">EXAMPLES</span></span>

### <span data-ttu-id="5e14f-113">Exemplo 1: Remover um tipo de conexão</span><span class="sxs-lookup"><span data-stu-id="5e14f-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5e14f-114">Este comando remove um tipo de conexão chamado ContosoConnectionType na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5e14f-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5e14f-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5e14f-115">PARAMETERS</span></span>

### <span data-ttu-id="5e14f-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5e14f-116">-AutomationAccountName</span></span>
<span data-ttu-id="5e14f-117">Especifica o nome da conta de automação para a qual esse cmdlet remove um tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="5e14f-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e14f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e14f-118">-DefaultProfile</span></span>
<span data-ttu-id="5e14f-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5e14f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e14f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5e14f-120">-Force</span></span>
<span data-ttu-id="5e14f-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="5e14f-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e14f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5e14f-122">-Name</span></span>
<span data-ttu-id="5e14f-123">Especifica o nome do tipo de conexão de automação que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="5e14f-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e14f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e14f-124">-ResourceGroupName</span></span>
<span data-ttu-id="5e14f-125">Especifica o nome do grupo de recursos do qual este cmdlet remove um tipo de conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="5e14f-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e14f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e14f-126">-Confirm</span></span>
<span data-ttu-id="5e14f-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e14f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e14f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e14f-128">-WhatIf</span></span>
<span data-ttu-id="5e14f-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e14f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e14f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e14f-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e14f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e14f-131">CommonParameters</span></span>
<span data-ttu-id="5e14f-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e14f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e14f-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e14f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e14f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e14f-134">INPUTS</span></span>

### <span data-ttu-id="5e14f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5e14f-135">System.String</span></span>

## <span data-ttu-id="5e14f-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5e14f-136">OUTPUTS</span></span>

### <span data-ttu-id="5e14f-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="5e14f-137">System.Void</span></span>

## <span data-ttu-id="5e14f-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="5e14f-138">NOTES</span></span>

## <span data-ttu-id="5e14f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e14f-139">RELATED LINKS</span></span>

[<span data-ttu-id="5e14f-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5e14f-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


